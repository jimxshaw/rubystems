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
