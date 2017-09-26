# Ruby
- inspired by Kevin Skoglund's Lynda course: **Introducing Ruby**

## Getting Started with Ruby

What is the definition of Ruby according to `man ruby`?
- Interpreted object-oriented scripting language

Who created Ruby?
- Yukihiro Matsumoto

What year was Ruby invented?
- 1995

How is Yukihiro Matsumoto referred to in the Ruby community?
- Matz

True or false: Ruby is a compiled language.
- false

True or false: Ruby is whitespace independent.
- true

What does the acronym MINASWAN stand for?
- Matz is nice and so we are nice.

How can you check for your version of Ruby in the shell?
- `ruby -v`
- `ruby --version`

What shell command will show you the path where your Ruby program is located?
- `which ruby`

What are the 3 ways to execute a Ruby command or program?
- single command
- Ruby file
- IRB

How do you prefix your single commands from the shell?
- `ruby -e`

What characters do you surrond your single line ruby code with?
- single parentheses

Which of the following represents a single line Ruby command?
- `ruby -e 'puts 123'`

What file extension is used for Ruby files?
- `.rb`

What is the long form file extension for Ruby files?
- `.ruby`

From the shell, how would you execute the file `execute_me.rb`?
- `ruby execute_me.rb`

How do you make a single line comment in Ruby?
- `#`

What does IRB stand for?
- `Interactive Ruby Shell`

From the shell, what command will put you into IRB mode?
- `irb`

What is the return value of `puts 999`?
- `nil`

How do you exit an IRB session?
- `quit`

How do start an IRB session with a simple prompt?
- `irb --simple-prompt`

How can you open the Ruby documentation from the shell?
- `ri <command>`

What does `ri` stand for?
- ruby information

## Ruby Object Types

In Ruby, is a variable an object?
- false, acts like an object, but is really a pointer or representation of an actual object

How are variables named in Ruby?
- starting with a letter or underscore, conventionally all lowercase

What are naming conventions for Ruby variables?
- readable, eg `articles_written` vs `aw_counter`

What scope does `$variable` have?
- global

What scope does `@@variable` have?
- class

What scope does `@variable` have?
- instance

What scope does `variable` have?
- local, or block

In Ruby 2.4.1, what class does `255.class` return?
- Integer

In Ruby 2.4.1, what class does `9.99.class` return?
- Float

What does `10 / 3` return?
- `3`

What method will turn `12345.6789` to `12346`?
- `#round`

What method will turn a number of type Float into an integer?
- `#to_i`

What is the return value of `10.to_f`?
- `10.0`

What method will always round down `12345.6789` down to `12345`?
- `#floor`

What method will always round down `12345.6789` up to `12346`?
- `#ceil`

Why is a string called a string?
- sequence of characters that you string together

What will the return value be of `"Hello"`?
- `"Hello"`

What will the return value be of `'Hello'`?
- `"Hello"`

What will the expression `'1' * 5` return?
- `"11111"`

How would you escape the apostrophe using a single-quoted string, `'I'm escaped.`?
- `'I\'m escaped.`

What does the command `puts '\ta\tb\nc\nd'` return?
- nil

What does the command `puts '\ta\tb\nc\nd'` output?
- `\ta\tb\nc\nd`

Would you use double quotes or single quotes for `\n` to be processed as a new line?
- double quotes

Would you use double quotes or single quotes when using interpolation?
- double quotes

What command can you call on "hello" to return "olleh"?
- `"hello".reverse`

What command can you call on "hello" to return "Hello"?
- `"hello".capitalize`

What command can you call on "HELLO" to return "hello"?
- `"HELLO".downcase`

What command can you call on "hello" to return "HELLO"?
- `"hello".upcase`

What method will return the number of characters in a string?
- `#length`

Given that double quotes are used to process special characters like `\n`, what value does `"\never".length` return?
- 5

What is an ordered, integer-indexed collection of any object?
- Array

What is the default starting index value for an array in Ruby?
- `0`

Given that `alpha = ['b', 'e', 't']`, what does `alpha[1]` return?
- `"e"`

How would you change the 'e' to an 'i'?
- `alpha[1] = "i"`

How would you append an "e" onto the array as a new element?
- `alpha << "e"`

What method can you call on your array to remove all the elements and return an empty array?
- `alpha.clear`

What is the difference between `alpha.clear` and `alpha = []`?
- `#clear` retains the object_id and is presumably more memory efficient

What does calling the `#inspect` method on an array return?
- a human readable representation of the array

Given that `one_thru_five = [1, 2, 3, 4, 5]`, what does `one_thru_five.inspect` return?
- `"[1, 2, 3, 4, 5]"`

Given that `crazies = [1, "2", ["hey", "you"], 5.0]`, what is the advantage of using `#inspect` in the command: `puts crazies.inspect`?
- keeps the array in human readable form

What would the return value of `crazies.to_s` be in Ruby 2.4.1?
- `"[1, \"2\", [\"hey\", \"you\"], 5.0]"`

What would the return value of `crazies.to_s` be in Ruby XXX?
- `"12heyyou5.0"`

What does `crazies.join` return?
- `"12heyyou5.0"`

What method would you use to reverse an elements arrays?
- `#reverse`

What array method would list an array of integers from lowest to highest value?
- `#sort`

What array method would return an array of unique values?
- `#uniq`

How would you remove the first element from `one_thru_five`?
- `one_thru_five.delete_at(0)`

How would you remove every occurence of the value `5` in `one_thru_five`?
- `one_thru_five.delete(5)`

What's another way to remove every occurence of the value `5`?
- `one_thru_five - [5]`

What's the difference in the two methods?
- `#delete()` mutates `self`, whereas subtraction leaves `self` intact and simply returns a new array.

What is an unordered, object-indexed collection of objects?
- Hash

For most cases, when should you use an Array?
- when order matters

For most cases, when should you use a Hash?
- when label matters

Square brackts `[]` are to an Array as ? is to a Hash.
- `{}` angle brackets

What is the new method that replaced the deprecated `#index()` as in `Hash.index()`?
- `Hash#key()`

What warning will be shown if you try to use `Hash.index()`?
- `warning: Hash#index is deprecated; use Hash#key`

Given the hash `hash = {a: 1, b: 2, c: 3}`, what will `hash.keys` return?
- `[:a, :b, :c]`

Given the hash `hash = {a: 1, b: 2, c: 3}`, what will `hash.values` return?
- `[1, 2, 3]`

Given the hash `hash = {}`, what will both `hash.keys` and `hash.values` return?
- `[]`

Can you use integers as hash keys, but as pure symbols, eg `:1`?
- false

What data type is a label used to identify a piece of data?
- Symbol

What is the punctuation that denotes the use of a symbol?
- colon `:`, as in `:symbol`

What is the assignment operator?
- `=`

What operator checks for value equality?
- `==`

What operator checks for value and type equality?
- `===`

When method names end in a question mark, as in `#empty?`, they will typically return what data type?
- Boolean

What is the return value of `(1..10).class`?
- Range

What is an example of an inclusive range, 1, 2, ..., 10?
- 1..10

What is an exclusive range that returns 1, 2, ..., 10?
- 1...11

Given an inclusive range, 1 thru 10 (1..10), what method will return the first number?
- (1..10).begin

Given an inclusive range, 1 thru 10 (1..10), what method will return the last number?
- (1..10).end

Given an exclusive range, what will (1...10).end result in?
- 10

For range methods, begin is to first as end is to what?
- last

How can you convert a range to an array?
- use the splat operator, `*`

Given that `x = 1..3`, what does `[*x]` return?
- `[1, 2 ,3]`

Given that `alpha = "a".."c"`, what does `[*alpha]` return?
- `["a", "b", "c"]`

Are Ruby constants objects?
- not true objects; act more like variables (pointers/representations but immutable). Are they frozen?

How are constants different from variables?
- First letter capitalized. Cannot start with underscore.

True or false: Ruby constants are immutable.
- false, assigning a new value will give warning, but will occur nonetheless

How can you make a constant (or other variable) immutable?
- `#freeze`

## Control Structures

True or false: `if` statements must be closed by the `end` keyword.
- true

How do you add additional condition expressions?
- `elsif`

Do you include the 'e' in your 'else if' statement?
- no

How can you rewrite `if true; true; end;`?
- `true if true`

How would you write `if true; true; else false; end` using the ternary operator?
- `true ? true : false`

What is the shorthand for `if !true; # do something; end`?
- `unless true;`

What is a switch statement called in Ruby?
- Case

What's a shorthand way of writing `if y; x = y; else x = z; end;`?
- `x = y || z`

What's a shorthand way of writing `unless x; x = y; end`?
- `x ||= y`

True or false: `loop do ... end` represents a loop structure.
- true

What loop keyword will terminate the entire loop when executed?
- break

What loop keyword will jump to the next loop?
- next

What loop keyword will repeat the same loop?
- redo

Which loop keyword will start the entire loop over?
- retry

True or false: you have to manually control your looping condition in a for loop.
- true

True or false: you have to manually control your looping condition in an until and while loop.
- false; condition is built into the loop

Do `while` and `until` loops begin with a `do` statement?
- false

What's the one-line while loop provided you've previously defined your starting counter?
- `x += 2 while x < 100`

What's the difference in a loop and an iterator?
- breaking out of a loop requires a condition, whereas iterating is looping over a fixed set of data

What's the simplest iterator?
- `n.times {...}` where `n` is an integer

What are similar iterators to the above?
- `1.upto(5) {...}`
- `5.downto(1) {...}`
- `(1..5).each {...}`

How would you specify the local variable to access elements you're looping over?
- `(1..5).each {|n|...}`

Given that `letters = ["a", "b", "c"]`, what is the equivalent for loop of `letters.each { |letter| ... }`?
- `for letter in letters`

## Code Block

What keywords *commonly* define a multi-line code block?
- `do` and `end`

What symbols (word!) *commonly* define a single-line code block?
- `{` and `}`

How would you use `do` and `end` in a single line to refactor `5.times { puts "Hello" }`?
- `5.times do; puts "Hello"; end`

Given a block scope `{|i| puts i}`, is the block variable `i` accessible in the local scope?
- false

True or false: local variables are available inside block scope.
- true

If a local variable and block variable have the same name, which variable will be used in the block scope?
- block

What are the five most common methods used in blocks?
- find (detect), merge, collect (map), sort, and inject

What is the synonym for the method `find`?
- `detect`

What is the synonym for the method `find_all`?
- `select`

Given a range or array of objects, `find` or `detect` will return what value?
- the first that satisfies block's criteria

What is returned from `find` if it detects nothing?
- `nil`

The `find_all` method will return all values that satisfy the block's criteria and return what data type?
- Array

Even if `find_all` effectively `detect`s a single occurence, what will it return?
- a single element in an array

True or false: `find_all` will return `nil` if no occurence is found.
- false, will return an empty array

What is the synonym for `find_all`?
- `select`

What is the boolean equivalent to `find` and `detect`?
- `any?`

How can you test if every element in an array satisfies a block's conditions?
- `all?`

True or false: `delete_if` will only work on arrays.
- true, will not work on a range (splat to array first)

Given that `h1 = { a: 1 }` and `h2 = { a: 2 }`, what does `h1.merge(h2)` return?
- `{ a: 2 }`

Given that `h1 = { a: 1 }` and `h2 = { a: 2 }`, what does `h2.merge(h1)` return?
- `{ a: 1 }`

Using `#merge()` with a code block uses what three block variables?
- key, old, new

Does the `#merge()` method mutate the object it operates on?
- false, use bang if you want that behavior

True or false: it is impossible to return an array of different length using `map` or `collect`.
- true

Given `hash = { a: 1, b: 2 }`, how can you express `hash.keys` using `map`?
- `hash.map {|k,v| k}`

Even though `map` can used on a Range, Array, and Hash, what is its return value data type?
- Array

What is the comparison operator, sometimes called a "spaceship" operator?
- `<=>`

Given the comparison `a <=> b`, what is returned when `a < b`?
- `-1`

Given the comparison `a <=> b`, what is returned when `a == b`?
- `0`

Given the comparison `a <=> b`, what is returned when `a > b`?
- `1`

What is returned for the comparison `Numeric <=> Integer`?
- `1`

What is returned for the comparison `Integer <=> Numeric`?
- `-1`

What is returned for the comparison `Integer <=> Float`?
- `nil`

How can you further specify the sort details in an Array?
- `array.sort { |a, b| a <=> b }`

When sorting a Hash, what does the hash effectively become upon sort?
- an array whose elements are two-element arrays, where arr[0] is the key and arr[1] is the value.
- `[ [:a, 1], [:b, 2], [:c, 3] ]`

Inject is an accumulator whose block variable is commonly called what?
- memo

What is the alias for `#inject`?
- `#reduce`

How can you set the starting value when using inject?
-`array.inject(100) {|memo,n|memo+n}`

You can compare all values in an array and return one of interest...
- inject/reduce and memo

## Methods

What two three-letter words come before and after the method name when defining a method?
- `def` and `end`

What statement in IRB will grant you access to use the methods in a Ruby file, eg `my_ruby_file.rb`?
- `require 'my_ruby_file.rb'`

Given the following method definition, what is the scope of the `value` variable?
```ruby
def over_five?
  value = 3
  puts value > 5 ? 'Over 5' : 'Not over 5'
end
```
- local

True or false: moving the `value = 3` expression outside of the method will still work.
- false, `value` would be local to the working space, and would not "bleed over" or "reach into" the method.

Will the following method work?
```ruby
@value = 7
def over_five?
  puts @value > 5 ? 'Over 5' : 'Not over 5'
end
```
- true

What is a comma-separated list of values passed into a method called?
- arguments

What is the shorthand for arguments?
- `args`

Do methods that take arguments typically have parentheses?
- true

Do methods that take no arguments typically have parentheses?
- false

True or false: passing arguments to a method requires the use of parentheses.
- false

True or false: arguments passed into a method are considered block variables.
- false, they become local to the method

In the error `ArgumentError: wrong number of arguments (given 0, expected 1)`, what does the `given 0` part mean?
- the method was called without passing in arguments

If you call a method without passing an argument and don't get the ArgumentError, what happened?
- the argument in the method definition has a default value set

How do define a default value in an argument?
- `arg="my_default_value"`

What is the common sense default ordering of required and default arguments?
- required are listed first, then default args

True or false: running a `return` statement inside a method when called will exit the method.
- true

True or false: `return x, y` will produce the same result as `return [x, y]`
- true

How can you use double assignment on the following code?
```ruby
arr = [1, 2]
one = arr[0]
two = arr[1]
```
- `one, two = arr`

How would you explicitly call the plus method on a number (syntactic vinegar)?
- `8.+(2)`

How would you call the shovel method vinegarly?
- `arr.<<(4)`

What is the name of the method used in `array[2]`?
- square-bracket, square-bracket

How would you explicitly call the sq-br-sq-br method?
- `array.[](2)`

How would you convert the following to syntactic vinegar? `array[2] = 'x'`
- `array.[]=(2, 'x')`

Why can't you do vinegar sugar on variable assignment, like so: `var.=(5)`?
- methods can only be called on objects and variable only represent (or point to) objects

## Classes

If `def` is used to define methods, what word is used to define classes?
- `class`

How does naming differ between methods and classes?
- methods are snake_case, and classes are PascalCase

When you instantiate an object from a class, what is that object called?
- instance

What is a value that persists inside of an instance?
- attribute

Why can't instance variables be accessed without using a method?
- Objects cannot call a variable; they can only call methods

What is another word pair to define "getter/setter" methods?
- reader/writer

When running `product.shipping_address = "211 N Ervay"`, are you setting the variable `shipping_address` or calling the method `#shipping_address()`?
- `#shipping_address()`

What is the Ruby equivalent to declare a setter method:
```ruby
def set_shipping_address(shipping_address)
  @shipping_address = shipping_address
end
```
- `def shipping_address=(shipping_address)`

What are the three most common Ruby attribute methods?
- attr_`reader`, `writer`, and `accessor`

What is Ruby's constructor function called?
- initialize

If you have `def initialize(a, b, c)`, how do you pass values (parameters) into the constructor as args?
- `Class.new(a_value, b_value, c_value)`

What is the most common class method built in?
- `Class.new`

How would you distinguish between an instance method `#instance` and a class method `.class`?
- `def self.method_name`

In a class definition, where would you typically find class methods?
- above instance methods

True or false: attribute reader, writer, and accessor *will* work on class variables.
- false

How would you define class readers and writers (getters and setters)?
- `def self.name; @@name` and `def self.name=(name="classy"); @@name = name`

The meaning of `self` in a method changes its meaning based on the method type. `self` is less dynamic in a class method (always referring to the class itself... just trickles the class name really). `self` in an instance method won't have meaning until the class is instantiated. Then `self` becomes the instance in the form of an object.
- test for `self`

What character indicates class inheritance?
- `<`

On which side of the `<` character does the class name go?
- left, as in `class ClassName < InheritFromMe`

True or false: a Ruby class can inherit from multiple parent classes.
- false

What's wrong with this class definition? `def SubClass < ParentClass`
- `def` instead of `class`

If `class Parent; def method; puts "parent"` and `class Child < Parent; def method; super` what does `super` do?
- it calls `Parent#method`; `super` is a method call so it's not entirely akin to `self`

