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

