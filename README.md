RSpec Rails Examples
====================

Rails app with examples of how to test with RSpec and other testing gems.

<!-- MarkdownTOC depth=0 autolink=true bracket=round -->

- [Testing Rake Tasks with RSpec](#testing-rake-tasks-with-rspec)
- [Pry-rescue debugging](#pry-rescue-debugging)
- [Time Travel Examples](#time-travel-examples)
- [Database Cleaner Examples](#database-cleaner-examples)
- [Factory Girl Examples](#factory-girl-examples)
- [Capybara Examples](#capybara-examples)
- [Shoulda-Matchers Examples](#shoulda-matchers-examples)
- [Email-Spec Examples](#email-spec-examples)
- [Devise Examples](#devise-examples)
- [RSpec-Expectations Docs](#rspec-expectations-docs)
- [RSpec-Mocks Specs & Docs](#rspec-mocks-specs--docs)
- [RSpec-Rails](#rspec-rails)
  - [Matchers](#matchers)
  - [Generators](#generators)
  - [Feature Specs & Docs](#feature-specs--docs)
  - [Mailer Specs & Docs](#mailer-specs--docs)
  - [Controller Specs & Docs](#controller-specs--docs)
  - [Helper Specs & Docs](#helper-specs--docs)
  - [Routing Specs & Docs](#routing-specs--docs)
- [Contributors](#contributors)

<!-- /MarkdownTOC -->

# Testing Rake Tasks with RSpec

RSpec testing Rake task example:
- [spec/tasks/subscription_tasks_spec.rb](spec/tasks/subscription_tasks_spec.rb)

# Pry-rescue debugging
pry-rescue can be used to debug failing specs, by opening pry's debugger whenever a test failure is encountered. For setup and usage see [pry-rescue's README](https://github.com/ConradIrwin/pry-rescue).


# Time Travel Examples
[`ActiveSupport::Testing::TimeHelpers`](http://api.rubyonrails.org/classes/ActiveSupport/Testing/TimeHelpers.html) provides helpers for manipulating and freezing the current time reported within tests. These methods are often enough to replace the time-related testing methods that the `timecop` gem is used for.

`TimeHelpers` configuration how-to and examples:
- [spec/support/time_helpers.rb](spec/support/time_helpers.rb)
- [spec/models/subscription_spec.rb](spec/models/subscription_spec.rb)
- [spec/tasks/subscription_tasks_spec.rb](spec/tasks/subscription_tasks_spec.rb)
- [`travel_to`](http://api.rubyonrails.org/classes/ActiveSupport/Testing/TimeHelpers.html#method-i-travel_to) example: [spec/models/subscription_spec.rb](spec/models/subscription_spec.rb)
- [`ActiveSupport::Testing::TimeHelpers` API documentation](http://api.rubyonrails.org/classes/ActiveSupport/Testing/TimeHelpers.html)


# Database Cleaner Examples

[Database Cleaner](https://github.com/DatabaseCleaner/database_cleaner) is a set of strategies for cleaning your database in Ruby, to ensure a consistent environment for each test run.

Database Cleaner configuration how-to:
- [spec/support/database_cleaner.rb](spec/support/database_cleaner.rb)


# Factory Girl Examples

[Factory Girl](https://github.com/thoughtbot/factory_girl) is a library to help setup test data. [factory_girl_rails](https://github.com/thoughtbot/factory_girl_rails) integrates Factory Girl with Rails.

Factory Girl configuration how-to and examples:
- [spec/support/factory_girl.rb](spec/support/factory_girl.rb)
- [spec/factories](spec/factories)
- [spec/factories/users.rb](spec/factories/users.rb)
- [spec/models/subscription_spec.rb](spec/models/subscription_spec.rb)
- [spec/tasks/subscription_tasks_spec.rb](spec/tasks/subscription_tasks_spec.rb)
- [spec/features/user_login_and_logout_spec.rb](spec/features/user_login_and_logout_spec.rb)


# Capybara Examples

[Capybara](https://github.com/jnicklas/capybara) helps you write feature specs that interact with your app's UI as a user does with a browser.

Capybara configuration how-to and examples:
- [spec/support/capybara.rb](spec/support/capybara.rb)
- [spec/features/home_page_spec.rb](spec/features/home_page_spec.rb)
- [spec/features/subscribe_to_newsletter_spec.rb](spec/features/subscribe_to_newsletter_spec.rb)
- [spec/features/user_login_and_logout_spec.rb](spec/features/user_login_and_logout_spec.rb)
- [spec/features/user_registers_spec.rb](spec/features/user_registers_spec.rb)
- [Capybara cheatsheet](https://gist.github.com/zhengjia/428105)
- [Capybara matchers](http://www.rubydoc.info/github/jnicklas/capybara/master/Capybara/Node/Matchers)

# Shoulda-Matchers Examples

[Shoulda-matchers](https://github.com/thoughtbot/shoulda-matchers) make light work of model specs.

shoulda-matchers configuration how-to and examples:
- [spec/support/shoulda-matchers.rb](spec/support/shoulda-matchers.rb)
- [spec/models/subscription_spec.rb](spec/models/subscription_spec.rb)


# Email-Spec Examples

The "Subscribe to newsletter" feature was developed with help from [email_spec](https://github.com/bmabey/email-spec)

email_spec configuration how-to and examples:
- [spec/support/email_spec.rb](spec/support/email_spec.rb)
- [spec/mailers/subscription_mailer_spec.rb](spec/mailers/subscription_mailer_spec.rb)
- [spec/features/subscribe_to_newsletter_spec.rb](spec/features/subscribe_to_newsletter_spec.rb)
- [spec/features/user_registers_spec.rb](spec/features/user_registers_spec.rb)


# Devise Examples

Specs testing registration, sign-in, and other user authentication features provided by Devise:

- [spec/features/user_login_and_logout_spec.rb](spec/features/user_login_and_logout_spec.rb)
- [spec/features/user_registers_spec.rb](spec/features/user_registers_spec.rb)


# RSpec-Expectations Docs
- [RSpec-Expectations API](http://www.rubydoc.info/gems/rspec-expectations/frames)
- [RSpec-Expectations matchers](https://www.relishapp.com/rspec/rspec-expectations/docs/built-in-matchers)


# RSpec-Mocks Specs & Docs
- [spec/controllers/subscriptions_controller_spec.rb](spec/controllers/subscriptions_controller_spec.rb)
- [spec/mailers/subscription_mailer_spec.rb](spec/mailers/subscription_mailer_spec.rb)
- [spec/models/subscription_spec.rb](spec/models/subscription_spec.rb)
- [RSpec Mocks API](https://relishapp.com/rspec/rspec-mocks/v/3-1/docs)

# RSpec-Rails
See [RSpec Rails](https://relishapp.com/rspec/rspec-rails/v/3-1/docs) for installation instructions.

## Matchers
- https://relishapp.com/rspec/rspec-rails/v/3-1/docs/matchers

## Generators
- https://relishapp.com/rspec/rspec-rails/v/3-1/docs/generators

## Feature Specs & Docs
- [spec/features/subscribe_to_newsletter_spec.rb](spec/features/subscribe_to_newsletter_spec.rb)
- [Feature specs API](https://relishapp.com/rspec/rspec-rails/v/3-1/docs/feature-specs/feature-spec)

## Mailer Specs & Docs
- [spec/mailers/subscription_mailer_spec.rb](spec/mailers/subscription_mailer_spec.rb)
- [Mailer specs API](https://relishapp.com/rspec/rspec-rails/v/3-1/docs/mailer-specs/url-helpers-in-mailer-examples)

## Controller Specs & Docs
- [spec/controllers/subscriptions_controller_spec.rb](spec/controllers/subscriptions_controller_spec.rb)
- [Controller specs API](https://relishapp.com/rspec/rspec-rails/v/3-1/docs/controller-specs)
- [Controller specs cheatsheet](https://gist.github.com/eliotsykes/5b71277b0813fbc0df56)

## Helper Specs & Docs
- [spec/helpers/application_helper_spec.rb](spec/helpers/application_helper_spec.rb)
- [Helper specs API](https://relishapp.com/rspec/rspec-rails/v/3-1/docs/helper-specs/helper-spec)

## Routing Specs & Docs
- [spec/routing/subscriptions_routing_spec.rb](spec/routing/subscriptions_routing_spec.rb)
- [Routing specs API](https://relishapp.com/rspec/rspec-rails/v/3-1/docs/routing-specs)


---

# Contributors

- Eliot Sykes https://eliotsykes.com/
- Your name here, contributions are welcome and easy! Just fork the GitHub repo, make your changes, then submit your pull request!
