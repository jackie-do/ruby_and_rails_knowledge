# Major updates of Rails versions

You can check futher in section "Release Notes" of [Rails Guides](https://guides.rubyonrails.org/)

## Rails 5

- Rails 5 requires Ruby 2.2.2 or newer.

### 5.0

- Add module `Action Cable` - It integrates Websockets in Rails app, make implementing real-time features more easy.
- Support Api Only when generate Rails

  ```bash
  rails new my_api --api
  ```

- Improve Active Record attributes API
  - Use method `attribute` to override types and default values of attributes in ActiveRecord (normally, type and default values set via schema.rb)
  - an `attribute` doesn't need to stick with a column in database

### 5.1

- Support `Yarn` to manange Javascript dependencies
- Support `Webpack` as a Javascript asset bundler
- Encrypted secrets, Secrets will be decrypted in production, using a key stored either in the `RAILS_MASTER_KEY` or file `<environment>.key`

  ```bash
  bin/rails secrets:setup
  ```

## Rails 6

- Rails 6 requires Ruby 2.5.0 or newer

### 6.0

- Add a new task for update Rails version. After updating the Rails version in the `Gemfile` run command

  ```bash
  rails app:update
  ```

- Load code in mode `zeitwerk` (the old one is `classic`), require file structure more strictly
- Add module `ActionMailbox` - allows you to route incoming emails to controller-like mailboxes
- Add module `Action Text` - brings rich text content and editing to Rails (Normally used in Rails View)
- Support Parallel Testing
- Support Action Cable Testing

### 6.1


## Rails 7

## Rails 8
