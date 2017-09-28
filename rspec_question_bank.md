# RSpec
- figured I might as well generate some stems for RSpec while taking [Ruby: Testing with RSpec](https://www.lynda.com/Ruby-tutorials/RSpec-Testing-Framework-Ruby/183884-2.html)

## Intro

What is RSpec stand for?
- Ruby Specification

What is the user story structure?
- Given, when, then

What is the minimum version of Ruby required to use RSpec?
- Ruby 1.8.7

True or false: RSpec is part of the Ruby Standard Library.
- false

## Installation

What command will bring up the help menu for RSpec?
- `rspec --help`

What does `rspec --version` return?
```bash
RSpec 3.6
  - rspec-core 3.6.0
  - rspec-expectations 3.6.0
  - rspec-mocks 3.6.0
  - rspec-support 3.6.0
```

How do you install RSpec?
- `gem install rspec`

How do you update RSpec to the latest version?
- `gem update rspec`

What are the default configurations for RSpec?
- `--no-color`, `--format progress`, `--no-profile`, `--no-fail-fast`, `--order defined`

Where is the global RSpec dotfile located on a Mac?
- `~/.rspec`

Where would you put a local RSpec config dotfile?
- working directory

True or false: teams do not check in `./.rspec` to source control.
- false, it is shared among team members

How would you specify your local `.rspec` file in addition to the project's `.rspec` file?
- `./.rspec-local`

## First Steps and Concepts

From your working directory, what command will initialize RSpec?
- `rspec --init`

What is created from the RSpec initialization?
- a `.rspec` file, and `spec` folder with `spec_helper.rb` therein

What text is by default in the project's `.rspec` file?
- `--require spec_helper`

If you have a Car class defined in `car.rb`, what should your RSpec file be named?
- `car_spec.rb`

Inside your spec file, how do you associate the spec file with the file it's testing against?
- `require '<some_file>'`

If the keyword `def` defines a method in Ruby, what keyword defines a test in RSpec?
- `describe`

What is a synonym for the keyword `describe`?
- `context`

The `describe` definition can take how many arguments?
- one

What type of objects can `describe`'s arguments be?
- `String` or `Class`

True or false: using `describe` *always* takes a code block.
- true

If your top-level `describe` refers to the class, you can nest another `describe` block to refer to its method.
- true

Examples of behavior are written in the code block. What is the most common keyword to define an example?
- `it`

What is a synonym for the example keyword, `it`?
- `specify`

How many arguments does `it` take?
- one

What data type is `it`'s argument?
- `String`

True or false: the example for `it` is always enclosed in a code block.
- true

What is the format for a positive expectation?
- `expect().to()`

What is the format for a negative expectation?
- `expect().not_to()`

