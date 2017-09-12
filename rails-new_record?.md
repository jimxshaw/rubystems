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

Dependent question on the previous (as a series): The Model.find(:id) and Model.find_by_id(:id) indeed produce the same SQL query. But while the `#find` method will return either an object or an error, the `#find_by_id` method will return either an object or *what*?

a. nil
b. true
c. false
d. the object its called on

...

(maybe another dependent question) Given that no records have been created in some table, say Narrators, what is the error message in Rails 5.1 that the `#find` method would return?

a. ActiveError::IdNotFound: Couldn't find Narrator with 'id'=1
b. ActiveError::InvalidRecord: Couldn't find Narrator with 'id'=1
c. ActiveRecord::ObjectNotFound: Couldn't find Narrator with 'id'=1
d. ActiveRecord::RecordNotFound: Couldn't find Narrator with 'id'=1

...

The above illustrate more ways to create multiple choice questions. Asking a true/false question is not the same as asking if an expression will evaluate to `true` or `false`.
