# Ruby and Rails knowledge

## I. Ruby Web Frameworks

- [Rails](https://rubyonrails.org/) - The most famost Ruby framework for building websites and web apps
  - [Major updates of Rails versions](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/1_ruby_web_frameworks/rails/major_updates_of_rails_version.md.md)
  - Rails Components in Advances:
    - [Active Record Query](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/1_ruby_web_frameworks/rails/active_record_query.md.md)
    - [Action Cable](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/1_ruby_web_frameworks/rails/action_cable.md.md)
    - [Rails Engine](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/1_ruby_web_frameworks/rails/action_cable.md.md)
- [Hanami](https://guides.hanamirb.org/v2.0/introduction/getting-started/) - A new star, applied new theories for modern and performance Ruby framework
- [Sinatra](https://sinatrarb.com/intro.html) - The simplest and lightest framework with more than 2k lines of code, support very basic features.
- [Grape](https://github.com/ruby-grape/grape#what-is-grape) - Grape is a REST-like API framework for Ruby
- [Karafka](https://github.com/karafka/karafka) - Karafka is a Ruby and Rails multi-threaded efficient Kafka processing framework

## II. Architectures

### 1. Rails Architectures

#### a. Model-View-Controller (MVC)

- Default architecture of Rails
  - You can read more in [https://guides.rubyonrails.org](https://guides.rubyonrails.org)

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

#### 1. Model-View-Controller (MVC)

- Default architecture of Rails
  - You can read more in [https://guides.rubyonrails.org](https://guides.rubyonrails.org):


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
- Styling: <https://github.com/rubocop/rails-style-guide>
- Awesome Ruby: <https://github.com/markets/awesome-ruby>

## VI. Useful Gem list

 - [Gem list](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/7_gems/useful_gems.md)

## VII. Books and Articles

- **Ruby (Basic, Design Pattern, Refactor, Low Level...)**
    > - (Beginner) [Well Grounded Rubybist - 3rd](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Well%20grounded%20Rubyist%20-%203rd.pdf)
    > - (Beginner - Middle) [Practical Object-Oriented Design - 2nd](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Practical%20Object-Oriented%20Design%20-%202nd.pdf)
    > - (Beginner - Middle) [TDD in Ruby](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Test%20Driven%20Development%20in%20Ruby.pdf)
    > - (Beginner - Middle) [Ruby Best Practices](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Ruby%20Best%20%20Practices.pdf)
    > - (Middle) [Design Patterns in Ruby(2007)](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Design%20Patterns%20in%20Ruby%20(2007).pdf)
    > - (Middle - Advance) [Refactoring Ruby](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Refactoring%20Ruby.pdf)
    > - (Middle - Advance) [Metaprograming Ruby](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Metaprogramming%20Ruby%202nd.pdf)
    > - (Advance) [Ruby Under a Microscope](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Ruby%20Under%20a%20Microscope.pdf)
    > - (Advance) [Ruby Performance Optimization](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Ruby%20-%20Ruby%20Performance%20Optimization.pdf)

- **Rails (Basic, Structure, Scalability...)**
    > - (Beginner) [Learn Rails 5.2](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Rails%20-%20Learn%20Rails%205-2.pdf)
    > - (Beginner) [Rails 5 Test Prescriptions](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Rails%20-%20Rails%205%20Test%20Prescriptions.pdf)
    > - (Middle) [Modular Rails - The complete guide](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Rails%20-%20Modular%20Rails%20The%20Complete%20Guide%20to%20Modular%20Rails%20Applications.pdf)
    > - (Middle) [Service-Oriented Design with Ruby on Rails](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Rails%20-%20Service-Oriented%20Design%20with%20Ruby%20and%20Rails.pdf)
    > - (Middle) [Component Based Rails Applications](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Rails%20-%20Component%20Based%20Rails-Applications.pdf)
    > - (Advance) [Lean Publishing Growing Rails Applications in Practice](https://github.com/jackiedo91/ruby_and_rails_knowledge/blob/master/6_books/Rails%20-%20Lean%20Publishing%20Growing%20Rails%20Applications%20in%20Practice%20(2014).pdf)
