---
tags: rails active-record
---

Given the Rails model `Narrator`, does calling `Narrator.new.new_record?` return `true` or `false`?

a. true
b. false

...

Given the Rails model `Narrator`, run the following code from Rails Console:

```ruby
narrator = Narrator.new
narrator.new_record?
```

What will be the final return value?

a. true
b. false
c. nil
d. <#Narrator>

True or false? The following two lines of Rails code will produce the same SQL query:

```ruby
Narrator.find(1)
Narrator.find_by_id(1)
```

a. True
b. False

...

The above illustrate more ways to create multiple choice questions. Asking a true/false question is not the same as asking if an expression will evaluate to `true` or `false`.
