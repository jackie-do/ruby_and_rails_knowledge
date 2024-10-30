# Ruby and Rails knowledge

## I. Ruby

### 1. Web Frameworks

- [Rails](https://rubyonrails.org/) - The most famost Ruby framework for building websites and web apps
  - [Major updates of Rails versions](https://github.com/jackie-do/ruby_and_rails_knowledge/blob/master/1_ruby_web_frameworks/rails/major_updates_of_rails_version.md)
  - Rails Components in Advances:
    - [Active Record Query](https://github.com/jackie-do/ruby_and_rails_knowledge/blob/master/1_ruby_web_frameworks/rails/active_record_query.md)
    - [Action Cable](https://github.com/jackie-do/ruby_and_rails_knowledge/blob/master/1_ruby_web_frameworks/rails/action_cable.md)
    - [Rails Engine](https://github.com/jackie-do/ruby_and_rails_knowledge/blob/master/1_ruby_web_frameworks/rails/action_cable.md)
- [Hanami](https://guides.hanamirb.org/v2.0/introduction/getting-started/) - A new star, applied new theories for modern and performance Ruby framework
- [Sinatra](https://sinatrarb.com/intro.html) - The simplest and lightest framework with more than 2k lines of code, support very basic features.
- [Grape](https://github.com/ruby-grape/grape#what-is-grape) - Grape is a REST-like API framework for Ruby
- [Karafka](https://github.com/karafka/karafka) - Karafka is a Ruby and Rails multi-threaded efficient Kafka processing framework

### 2. Coding and Best Practices

- [Ruby Best Libraries/Tools](https://github.com/markets/awesome-ruby)
- [Ruby Style Guide](https://github.com/rubocop/ruby-style-guide)
- [Rails Style Guide](https://github.com/rubocop/rails-style-guide)

## II. Architectures

### 1. Rails Architectures

#### a. Model-View-Controller (MVC)

- Default architecture of Rails
  - You can read more in [https://guides.rubyonrails.org](https://guides.rubyonrails.org)
- This architecture belongs to Monolothic architecture. Normaly, we should modulize our code base on business units to improve the scalability in future.

#### b. Abstract Layers in Rails

- You can read the book `Layered Design for Ruby on Rails - Viladimir Dementyev` to know more:
  - Abtract Layers in Rails
  - Something default of Rails is not good enough
  - When Rails Abstracts are not enough
  - Custom to add more layers into Rails

#### c. Components based (Modularizing Rails)

- You can read the book `Components-Based Rails Applications - Stephan Hagemann` to know more:
  - Utilizing [Rails Engine](https://guides.rubyonrails.org/engines.html) to build Rails application with Component-Based
  - What is the benefits ?
    - Improved Communication of Intent
    - Improved Collaboration Among Developers
    - Improved Creation of Features
    - Improved Maintenance of the Application
    - Improved Comprehension of Application Parts

#### 2. Module

### 2. Service Oriented Architecture (SOA)

- SOA (Service Oriented Architecture) without the tears

  <https://www.youtube.com/watch?v=JrS5pWp29OI>

### 3. Microservices

- Hanami in Microservices - <https://www.useo.pl/blog/2021/07/trying-hanami-in-microservices>

### 4. Domain Driven Design (DDD)

- DDD and Hexagonal Architecture with Rails

  <https://www.slideshare.net/dwhelan/domain-driven-design-and-hexagonal-srchitecture-with-rails>

- Refactoring with hexagonal Rail (with example)

  <https://www.agileplannerapp.com/blog/building-agile-planner/refactoring-with-hexagonal-rails>

- Building Complex Domains in Rails (DDD with Rails)

  <https://speakerdeck.com/mikeabiezzi/build-complex-domains-in-rails>

- Demo <https://github.com/Creditas/ddd-rails-sample>

#### Rails Common

- Rails 4 Engines

  <http://tech.taskrabbit.com/blog/2014/02/11/rails-4-engines/>

- 7 Ways to decompose fat activerecord models

  <https://codeclimate.com/blog/7-ways-to-decompose-fat-activerecord-models/>

- How I Architected My Big Rails App for success

  <https://www.youtube.com/watch?v=uDaBtqEYNBo>

## III. Optimizations

- Check and optimize Rails <https://github.com/rails/rails-perftest>

## IV. Testing and Benchmark

- Test Code Coverage

  <https://docs.google.com/presentation/d/1eu2x8EAPOe6LG2DTjNk-GZiUJ8TBAZuhq9awg31HfSU/edit#slide=id.g872c0e3715_0_1737>

## V. Documents of some tools

- Arel doc: <https://jpospisil.com/2014/06/16/the-definitive-guide-to-arel-the-sql-manager-for-ruby.html>

## VI. Useful Gem list

- [Gem list](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/7_gems/useful_gems.md)

## VII. Books and Articles

- **Ruby (Basic, Design Pattern, Refactor, Low Level...)**
    > - (Beginner) [Well Grounded Rubybist - 3rd]
    > - (Beginner - Middle) [Practical Object-Oriented Design - 2nd]
    > - (Beginner - Middle) [TDD in Ruby]
    > - (Beginner - Middle) [Ruby Best Practices]
    > - (Middle) [Design Patterns in Ruby(2007)]
    > - (Middle - Advance) [Refactoring Ruby]
    > - (Middle - Advance) [Metaprograming Ruby]
    > - (Advance) [Ruby Under a Microscope]
    > - (Advance) [Ruby Performance Optimization]

- **Rails (Basic, Structure, Scalability...)**
    > - (Beginner) [Learn Rails 5.2]
    > - (Beginner) [Rails 5 Test Prescriptions]
    > - (Middle) [Modular Rails - The complete guide]
    > - (Middle) [Service-Oriented Design with Ruby on Rails]
    > - (Middle) [Component Based Rails Applications]
    > - (Advance) [Lean Publishing Growing Rails Applications in Practice]
