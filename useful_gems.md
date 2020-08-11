# Useful Gem List
## 1) Optimizations (Database, Memory...)
  > * `newrelic_rpm`- It provides you with deep information about the performance of your Rails or Ruby application as it runs in production and transmits 
  > * `fast_jsonapi` - serialization time is at least 25 times faster than Active Model Serializers
  > * `ruby-jmeter` - This gem lets you write test plans for JMeter
  > * `jemalloc` - Instant jemalloc injection into Ruby apps, for better performance and less memory.
  > * `active_record_doctor` - Active Record Doctor helps to keep the database in a good shape
  > * `lol_dba` - small package of rake tasks that scan your application models and displays a list of columns that probably should be indexed  
  > * `rails-perftest` - Performance testing a Ruby on Rails application.
  > * `ruby-prof` - It can help you track down methods that are either slow, allocate a large number of objects or allocate objects with high memory usage
  > * `bullet` - The Bullet gem is designed to help you increase your application's performance by reducing the number of queries it makes.
  
## 2) Server, Database, Architect, Coding Patterns
  > * `apartment` - Apartment provides tools to help you deal with multiple tenants in your Rails application
  > * `ffi` - Ruby-FFI is a gem for programmatically loading dynamically-linked native libraries, binding functions within them, and calling those functions from Ruby code. (Ruby work with C)
  > * `paper_trail` - Track changes to your models, for auditing or versioning. See how a model looked at any stage in its lifecycle, revert it to any version, or restore it after it has been destroyed.
  > * `ransack` - Ransack enables the creation of both simple and advanced search forms for your Ruby on Rails application.
  > * `ar-octopus` - Octopus is a better way to do Database Sharding in ActiveRecord.
  
  #### Coding Patterns
  > * `interactor` - Apply Interactor for coding
  > * `draper` - Apply Decorator for coding
  > * `dry-transaction` - Apply DRY style by using transactions
  > * `dry-validation` - Apply DRY style by using validations
  > * `dry-initializer` - Support params and options
  

## 3) Paralllel and Concurrent Processing
  > * `parallel` - Run any code in parallel Processes(> use all CPUs) or Threads(> speedup blocking operations).
  > * `eventmachine` - EventMachine is an event-driven I/O and lightweight concurrency library for Ruby
  > * `typhoeus` - Using native C library for making multiple HTTP request at sametime

## 4) Authentications and Authorizations
  > * `pundit` - Pundit provides a set of helpers which guide you in leveraging regular Ruby classes and object oriented design patterns to build a simple, robust and scaleable authorization system.
  > * `devise_invitable` - It adds support to Devise for sending invitations by email (it requires to be authenticated) and accept the invitation setting the password.
  > * `devise` - Devise is a flexible authentication solution for Rails based on Warden.
  > * `devise_token_auth` - Simple, multi-client and secure token-based authentication for Rails.
  > * `simple_token_authentication` -  Token authentication with Devise.
  > * `cancancan` - an authorization library for Ruby and Ruby on Rails which restricts what resources a given user is allowed to access.
  > * `rolify` - Very simple Roles library without any authorization enforcement supporting scope on resource object.
  > * `warden` - Warden is a Rack-based middleware, designed to provide a mechanism for authentication in Ruby web applications.
  > * `mechanize` - used for automating interaction with websites. Mechanize automatically stores and sends cookies, follows redirects, and can follow links and submit forms.
  > * `recaptcha` - This gem provides helper methods for the reCAPTCHA API.
  
## 5) Ruby Framework, CMS
  > * `grape` - Grape is a REST-like API framework for Ruby. It's designed to run on Rack or complement existing web application frameworks such as Rails and Sinatra by providing a simple DSL to easily develop RESTful APIs.
  > * `camaleon_cms` - Camaleon CMS is a dynamic and advanced content management system based on Ruby on Rails that adapts to your needs
  > * `spina` - Spina is a CMS for Rails 5.2. This guide is designed for developers with experience using Ruby on Rails.
  > * `administrate` - Administrate is a library for Rails apps that automatically generates admin dashboards.
  > * `solidus` - A free, open-source ecommerce platform that gives you complete control over your store.

## 6) Testing
  > * `capybara-screenshot` - Active Merchant is an extraction from the ecommerce system Shopify. Shopify's requirements for a simple and unified API to access dozens of different payment gateways with very different internal APIs was the chief principle in designing the library.
  > * `vcr` - Record your test suite's HTTP interactions and replay them during future test runs for fast, deterministic, accurate tests. HELP TEST THIRD PARTY via HTTP CALL
  > * `webmock` - Using with vrc. Library for stubbing and setting expectations on HTTP requests in Ruby.
  > * `puma-ngrok-tunnel` - For Demo, A plugin for puma that'll start a ngrok tunnel to your rails server when puma starts. 
  > * `simplecov` - SimpleCov is a code coverage analysis tool for Ruby. The overall coverage results for your projects, including all types of tests, Cucumber features, etc
  > * `rspec-rails` - brings the RSpec testing framework to Ruby on Rails as a drop-in alternative to its default testing framework, Minitest.
  > * `fasterer` - Fasterer will suggest some speed improvements which you can check
  
  
  > * `rswag-specs` - Rswag extends rspec-rails "request specs" with a Swagger-based DSL for describing and testing API operations 
  
  
  > * `rubocop` -
  > * `rubocop-performance` -
  > * `rubocop-rails` -
  > * `rubocop-rspec` -
  
  
  > * `mongoid-rspec` -
  

  
## 7) Payment
  > * `activemerchant` - Active Merchant is an extraction from the ecommerce system Shopify. Shopify's requirements for a simple and unified API to access dozens of different payment gateways with very different internal APIs was the chief principle in designing the library.
  > * `money-rails` - This library provides integration of the money gem with Rails.
  > * `stripe` - The Stripe Ruby library provides convenient access to the Stripe API from applications written in the Ruby language

## 8) Document
> * `rails-erd` - is a gem that allows you to easily generate a diagram based on your application's Active Record models. The diagram gives an overview of how your models are related. Having a diagram that describes your models is perfect documentation for your application.
> * `apipie-rails` - Apipie-rails is a DSL and Rails engine for documenting your RESTful API
> * `annotate` - Add a comment summarizing the current schema to the top or bottom (ActiveRecord models, Fixture files ...)


> * `rswag-api` - xxx
> * `rswag-ui` - xxx

## 9) Monitoring
  > * `brakeman` - Brakeman is a static analysis tool which checks Ruby on Rails applications for security vulnerabilities
  > * `bundler-audit` - Check gems: vulnerable versions,  insecure gem sources, Prints advisory information ...
  > * `dawnscanner` - Dawnscanner is a source code scanner designed to review your ruby code for security issues
  > * `rubycritic` - RubyCritic is a gem that wraps around static analysis gems such as Reek, Flay and Flog to provide a quality report of your Ruby code.
  
## 10) Additional Features
  > * `ruby-progressbar` - The ultimate text progress bar library for Ruby!
  > * `rpush` - Rpush aims to be the de facto gem for sending push notifications in Ruby
  > * `carrierwave` - provides a simple and extremely flexible way to upload files from Ruby applications. It works well with Rack based web applications, such as Ruby on Rails. 
  > * `state_machine` - support for creating state machines for attributes on any Ruby class
  > * `gretel` - Handle Breadcrumb in Ruby
  > * `paranoia` - Solf delete
  > * `multipart-post` - Adds a streamy multipart form post capability to Net::HTTP. Also supports other methods besides POST.
  > * `dotenv-rails` - Shim to load environment variables from .env into ENV in development.
  > * `net-sftp` - Net::SFTP is a pure-Ruby implementation of the SFTP protocol.
  > * `database_cleaner-mongoid` - Database cleaner for MongoID
  > * `config` - Config helps you easily manage environment specific settings in an easy and usable manner.


  
