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

How would you run all the RSpec tests located in `spec/car_spec.rb`?
- `rspec spec/car_spec.rb`

How would you override the default no-color output?
- `rspec spec/car_spec.rb --color`

What does a passing test output?
- number of examples as dots, time to finish, time to load, number of examples, and number of failures

If one of your examples fails, what happens to its green dot?
- `F`

What do the dots become if you specify `--format documentation`?
- nested `describe`s and `it`s

What does the `F` correspond to using `--format documentation`?
- `(FAILED - 1)`

What is the shorthand for `--format documentation`?
- `-f d`

What is the shorthand for `--format progress`?
- `-f p`

How would you format the test output as HTML?
- `-f h`

How about JSON?
- `-f j`

How would you run your tests in random order?
- `rspec spec/car_spec.rb --order random`

How can you repeat a randomly ordered test?
- RSpec will output the seed value in `Randomized with seed 36793` for example.

How can you see the time it took for each test to run?
- `rspec spec/car_spec.rb --profile`

What is the shorthand for `--profile`?
- `-p`

What is the option to abort further tests after one fails?
- `--fail-fast`

How can you specify a specific test to run?
- `rspec spec/car_spec.rb:7` where `:7` indicates the line number in the spec file

How would you specify additional lines discretely?
- `rspec spec/car_spec.rb:7:13:19:25`

True or false: specifying a line number will also run nested `context` and `it` statements.
- true

What is the additional output when you specify line numbers?
- `Run options: include {:locations=>{"./spec/car_spec.rb"=>[7, 13, 19, 25]}}`

How can you signify that a test is pending?
- leave off the `do ... end` code block; just have `it "does something"`

In progress format, a dot signifies passing and an F signifies failing. What character signifies Pending?
- `*`

In documentation format, what additional text denotes a pending test?
- `(PENDING: Not yet implemented)`

True or false: placing an `x` in front of `it` to make `xit` will change that test's status to Pending.
- true

What text denotes a Pending test with `xit`?
- `(PENDING: Temporarily skipped with xit)`

If you skip an entire block by putting an `x` in front of `describe` to make `xdescribe` what notice will output?
- `(PENDING: Temporarily skipped with xdescribe)`

How would you use the `skip` keyword to omit a test?
- place at top of code block

If you simply use the `skip` method with no arguments, what text will output as the reason why pending?
- `(PENDING: No reason given)`

How can you specify why you want to skip a particular test?
- `skip("Skipping because...")` or something like that; `skip()` takes a single argument

If you use `pending()` instead of `skip()` the rest of your code block will run.
- true

If your code block following `pending()` is passing otherwise, it will fail at runtime.
- true

If you have a failing test that you want to work on later, use `pending()` until you get it to pass.
- true

## Working with Expectations

In general, you should only have one expectation per example.
- true

If you have more than one expectation per example and the first expectation fails, the remaining expectations will also fail.
- false, their code never gets run

The infinitive verbs that are arguments to `.to()` are called what?
- matchers

What is the general form of the matcher?
- `expect(actual).to match(expected)`

What are the five types of matchers?
- equivalence, truthiness, numeric-comparison, collection, and observation

What is the RSpec version 2 deprecated `should` form of `expect(@count).to eq(3)`?
- `@count.should eq(3)`

Should you use `should` in your `it` statements?
- false, use active voice instead

What's a good alternative to `it "should return an array of names"`?
- `it "returns an array of names"`

Which comparison matcher does `eq()` most closely resemble?
- `==`, double equals (value and closeness equality)

What's another (less common) way to write `expect(x).to eq(1)`?
- `expect(x).to be == 1`

In the above example, the test would pass for `x = 1.0`. How would you test for exact value and type?
- `expect(x).to eql(1)`

How would you test for object identity?
- `expect(x).to equal(1)`

What is another way to test for object identity?
- `expect(x).to be(1)`

How would you test a comparison to be true or false?
- `expect(1 < 2).to be(true)`

How would you test `nil` to be falsey?
- `expect(nil).to be_falsey`

How could you test the existance of an object?
- `expect(@instance).to be_truthy`, basically not be nil

What is the deprecated form of `be_truthy` in RSpec 2?
- `be_true`

How would you check for something to be nil?
- `expect(nil).to be_nil` or `expect(nil).to be nil`

How can you check if the value 100 is greater than 99?
- `expect(100).to be > 99`

How can you check if 5 is within the range 3 to 5, inclusive?
- `expect(5).to be_between(3, 5).inclusive`

How can you check if 5 is NOT within the range 3 to 5, exclusive?
- `expect(5).not_to be_between(3, 5).exclusive`

How can you check if 100 is within 5 units of 105?
- `expect(100).to be_within(5).of(105)`; inclusive

How can you test your value to be within a range, eg expect 3 to be within 1..10.
- `expect(1..10).to cover(3)`

How can you test if the array `[1, 2, 3]` includes values `1` and `3`?
- `expect([1, 2, 3]).to include(1, 3)`

How can you test an array's first element?
- `expect([1, 2, 3]).to start_with(1)`

How can you test an array's last element?
- `expect([1, 2, 3]).to end_with(3)`

How can you test an array even if the elements aren't in the same order?
- `expect([1, 2, 3]).to match_array([3, 1, 2])`

If `include_all` was a matcher, what would its actualy alias be?
- `expect([1, 2, 3]).to contain_exactly(3, 1, 2)`

How can you test if a hash has a key/value pair?
- `expect(hash).to include(key: :value)`

How can you test if your `string = "Lynda"` matches a RegExp?
- `expect(string).to match(/^L.+a$/)`

True or false: regular expressions only work with strings, and NOT numbers.
- true (yikes!)

How can you check if an instance variable is an instance of a class?
- `expect(@instance).to be_instance_of(Class)`

What's the alias for `be_instance_of()`?
- `be_an_instance_of()`

How can you check if an instance variable is either an instance of a class or subclass?
- `be_kind_of()`, `be_a_kind_of()`, or `be_a()`

How can you check if an array is an array?
- `expect([1, 2, 3]).to be_an(Array)`

How can you check if an instance has an instance method?
- `expect(@instance).to respond_to(:i_method)`, so `@bob.first_name` should be a valid call

How can you check if an instance has attrs?
- `expect(@chemturion).to have_attributes(username: 'chemturion')`

What is the matcher of last resort?
- `expect().to satisfy({})`, where block should return boolean

Given a custom method, RSpec will generate a predicate matcher, eg `#visible?` becomes `be_visible`.
- true

What's the longform way of writing `expect(product).to be_visible`?
- `expect(product.visible)to be(true)`

What is RSpec's equivalent to `hash.has_key?(:city)` call?
- `expect(hash).to have_key(:city)`

What is the basic format for observation matchers?
- `expect {}.to()` or `expect do ... end.to()`

If `array = []`, how would you test if shoveling `1` changes `array.empty?` from `true` to `false`?
- `expect { array << 1 }.to( change(array, :empty?).from(true).to(false) )`

If Bob Smith wants to confirm his name change to Robert Smith, how would he do that?
- `expect do; bob.first_name = 'Robert'; end.to( change(bob, :full_name).from('Bob Smith').to('Robert Smith')`

How would you observe a non-object value changing? Eg, `x = 1`
- `expect { x += 1 }.to( change{x}.from(1).to(2) )`; `change` now takes a block instead of comma-sep'd args

How would you observe the above without the explicit beginning and ending values?
- `expect { x += 1}.to( change{x}.by(1) )`

What are the range checkers for the `by()` method?
- `by_at_least()` and `by_at_most()`

What is a synonym for `raise_error`?
- `raise_exception`

How can you observe if an action will raise an error?
- `expect { customer.delete }.to( raise_error )`; assuming associations shouldn't allow it

How can you expect a specific error to be raised?
- `expect { 1/0 }.to( raise_error(ZeroDivisionError) )`

How can you spot check an error message to contain a phrase?
- `expect { 1/0 }.to( raise_error.with_message(/divided/) )`

How can you observe that a given behavior will output a particular way?
- `expect { print 'hello' }.to( output.to_stdout )`

How can you observe that a given behavior will output something specifically in a particular way?
- `expect { print 'hello' }.to( output(/ll/).to_stdout )`

Where else besides `to_stdout` would you output errors?
- `to_stderr`

