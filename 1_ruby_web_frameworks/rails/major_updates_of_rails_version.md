# Major updates of Rails versions

You can check futher in section "Release Notes" of [Rails Guides](https://guides.rubyonrails.org/)

## Rails 5

- Rails 5 requires Ruby 2.2.2 or newer.

### 5.0 (June 2016)

- Add module `Action Cable` - It integrates Websockets in Rails app, make implementing real-time features more easy.
- Support Api Only when generate Rails

  ```bash
  rails new my_api --api
  ```

- Improve Active Record attributes API
  - Use method `attribute` to override types and default values of attributes in ActiveRecord (normally, type and default values set via schema.rb)
  - an `attribute` doesn't need to stick with a column in database

### 5.1 (May 2017)

- Support `Yarn` to manange Javascript dependencies
- Support `Webpack` as a Javascript asset bundler
- Encrypted secrets, Secrets will be decrypted in production, using a key stored either in the `RAILS_MASTER_KEY` or file `<environment>.key`

  ```bash
  bin/rails secrets:setup
  ```

### 5.2 (April 2018)

## Rails 6

- Rails 6 requires Ruby 2.5.0 or newer

### 6.0 (August 2019)

- Add a new task for update Rails version. After updating the Rails version in the `Gemfile` run command

  ```bash
  rails app:update
  ```

- Load code in mode `zeitwerk` (the old one is `classic`), require file structure more strictly
- Add module `ActionMailbox` - allows you to route incoming emails to controller-like mailboxes
- Add module `Action Text` - brings rich text content and editing to Rails (Normally used in Rails View)
- Support Parallel Testing
- Support Action Cable Testing

### 6.1 (December 2020)

- Support ability to switch connections per-database with method `connect_to` [Read more](https://github.com/rails/rails/pull/40370)

  ```ruby
  # Example
  ApplicationRecord.connected_to(shard: :shard1, role: :primary) do
    User.first # reads from ApplicationRecord shard1 primary
    Shard.first # reads from GlobalRecord default primary
  end
  ```

- Support horizontal sharding (same schema, multiple partitions)

  ```yml
  # database.yml config
  production:
    primary:
      database: my_database
    primary_shard_one:
      database: my_database_shard_one
  ```

  ```ruby
  # Model config
  class ApplicationRecord < ActiveRecord::Base
    self.abstract_class = true

    connects_to shards: {
      default: { writing: :primary },
      shard_one: { writing: :primary_shard_one }
    }
  end

  # How to use
  ActiveRecord::Base.connected_to(shard: :shard_one) do
      # Read from shard one
  end
  ```

- "Strict" Loading Associations. Add `#strict` to any record to prevent lazy loading of associations (use `preload`)
- "Delegated Types" is an alternative to single-table inheritance. [Read more](https://github.com/rails/rails/pull/39341)
- Destroy Associations Async - The ability for applications to destroy associations in a background job, `destroy_async`.

  ```ruby
  class Person < Application
    has_many :classes, dependent: :destroy_async
  end
  ```

## Rails 7

- Rails 7 requires Ruby 2.7. 0 or newer

### 7.0 (December 2021)

### 7.1 (October 2023)

- Generate Dockerfiles for new Rails applicatons
- Add `ActiveRecord::Base.normalizes` - declares an attribute normalization

  ```ruby
  class User < ActiveRecord::Base
    normalizes :email, with: -> email { email.strip.downcase }
    normalizes :phone, with: -> phone { phone.delete("^0-9").delete_prefix("1") }
  end

  user = User.create(email: " CRUISE-CONTROL@EXAMPLE.COM\n")
  user.email                  # => "cruise-control@example.com"

  User.normalize_value_for(:phone, "+1 (555) 867-5309") # => "5558675309"
  ```

- Add `ActiveRecord::Base.generates_token_for` - defines the generation of tokens for a specific purpose. Generated tokens can expire and can also embed record data

  ```ruby
  class User < ActiveRecord::Base
    has_secure_password

    generates_token_for :password_reset, expires_in: 15.minutes do
      # `password_salt` (defined by `has_secure_password`) returns the salt for
      # the password. The salt changes when the password is changed, so the token
      # will expire when the password is changed.
      password_salt&.last(10)
    end
  end

  user = User.first
  token = user.generate_token_for(:password_reset)

  User.find_by_token_for(:password_reset, token) # => user

  user.update!(password: "new password")
  User.find_by_token_for(:password_reset, token) # => nil
  ```

- Add `perform_all_later` to enqueue multiple jobs at once

  ```ruby
  # Enqueueing individual jobs
  ActiveJob.perform_all_later(MyJob.new("hello", 42), MyJob.new("world", 0))

  # Enqueueing an array of jobs
  user_jobs = User.pluck(:id).map { |id| UserJob.new(user_id: id) }
  ActiveJob.perform_all_later(user_jobs)
  ```

- Support "Composite primary keys" at both the database and application level. This feature is particularly beneficial for many-to-many relationships and other complex data models where a single column is insufficient to uniquely identify a record.

  ```ruby
  class TravelRoute < ActiveRecord::Base
    query_constraints :origin, :destination
  end


  class TravelRouteReview < ActiveRecord::Base
    belongs_to :travel_route, query_constraints: [:travel_route_origin, :travel_route_destination]
  end
  ```

- Introduce adapter for `Trilogy` for MySQL

  ```yml
  # database.yml config
  development:
    adapter: trilogy
    database: blog_development
    pool: 5
  ```

- Add `ActiveSupport::MessagePack` - a serializer that integrates with the `msgpack` gem.

  ```ruby
  ## Can be used as a message serializer ##
  # Globally
  config.active_support.message_serializer = :message_pack

  # Or individually:
  ActiveSupport::MessageEncryptor.new(secret, serializer: :message_pack)
  ActiveSupport::MessageVerifier.new(secret, serializer: :message_pack)
  ```

  ```ruby
  ## Cookies serializer ##
  # Globally
  config.action_dispatch.cookies_serializer = :message_pack
  ```

  ```ruby
  ## Cache serializer ##
  # Globally
  config.cache_store = :file_store, "tmp/cache", { serializer: :message_pack }

  # Or individually:
  ActiveSupport::Cache.lookup_store(:file_store, "tmp/cache", serializer: :message_pack)
  ```

- Introducing `config.autoload_lib` and `config.autoload_lib_once` for Enhanced Autoloading.
  This method is used to enhance the autoload paths of applications by including the lib directory, which is not included by default. Also, `config.autoload_lib(ignore: %w(assets tasks))` is generated for new applications.

- Active Record API for general async queries (BIG BOOM!!) - A significant enhancement has been introduced to the Active Record API, expanding its support for asynchronous queries [Readmore](https://github.com/rails/rails/pull/44446)
- Testing mode
  - Support pattern matching for JSON response.parsed_body
  - Extend response.parsed_body to parse HTML with Nokogiri

### 7.2 (August 2024)

- Require Ruby 3.1 or later
- Support "Development containers" configuration
- Add browser version guard by default - adds the ability to specify the browser versions that will be allowed to access all actions

  ```ruby
  class ApplicationController < ActionController::Base
    # Allow only browsers natively supporting webp images, web push, badges, import maps, CSS nesting + :has
    allow_browser versions: :modern
  end

  class ApplicationController < ActionController::Base
    # All versions of Chrome and Opera will be allowed, but no versions of "internet explorer" (ie). Safari needs to be 16.4+ and Firefox 121+.
    allow_browser versions: { safari: 16.4, firefox: 121, ie: false }
  end

  class MessagesController < ApplicationController
    # In addition to the browsers blocked by ApplicationController, also block Opera below 104 and Chrome below 119 for the show action.
    allow_browser versions: { opera: 104, chrome: 119 }, only: :show
  end
  ```

- Default Progressive Web Application (PWA) files - New directory for PWA `app/views/pwa`
- Add "omakase RuboCop" rules by default [Read More](https://github.com/rails/rubocop-rails-omakase)
- Add GitHub CI workflow by default to new applications
- Add Brakeman by default to new applications
- Set a new default for the Puma thread count - from 5 => 3
- Prevent jobs from being scheduled within transactions.
  A common mistake with Active Job is to enqueue jobs from inside a transaction, causing them to potentially be picked and ran by another process, before the transaction is committed, which result in various errors.

  ```ruby
  Topic.transaction do
    topic = Topic.create

    NewTopicNotificationJob.perform_later(topic)
  end

  class NewTopicNotificationJob < ApplicationJob
    self.enqueue_after_transaction_commit = :never
  end
  ```

- Support Per transaction commit and rollback callbacks

  ```ruby
  Article.transaction do |transaction|
    article.update(published: true)

    transaction.after_commit do
      PublishNotificationMailer.with(article: article).deliver_later
    end
  end

  # ActiveRecord::Base.current_transaction was also added to allow to register callbacks on it.
  Article.current_transaction.after_commit do
    PublishNotificationMailer.with(article: article).deliver_later
  end

  # for code that may run either inside or outside a transaction and needs to perform work after the state changes have been properly persisted.
  def publish_article(article)
    article.update(published: true)

    ActiveRecord.after_all_transactions_commit do
      PublishNotificationMailer.with(article: article).deliver_later
    end
  end
  ```

- Enable YJIT by default if running Ruby 3.3+ - It can provide significant performance improvements for Rails applications, offering **15-25%** latency improvements.
- Setup `jemalloc` in default Dockerfile to optimize memory allocation [Read More](https://www.speedshop.co/2017/12/04/malloc-doubles-ruby-memory.html)
- Support `ActiveRecord::Base.connection_pool.with_connection` to we can return database connection in a block (instead of a request like normal) [Read More](https://github.com/rails/rails/pull/51349)

## Rails 8
