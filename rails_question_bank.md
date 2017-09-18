How do you create a Rails application called MyApp from the command line with a MySQL database?
- rails new my_app -d mysql

What's the shorthand for `rails generate`?
- rails g

You use singular PascalCase for Model generation.
- True, eg `rails generate model MyModel`

How do you add attributes and their datatype in Rails generate?
- rails generate model Product name:string

What option flag do you use to omit automatic timestamp attributes?
- rails generate model Product --no-timestamps

How do you autopopulate the migration change method?
- rails generate migration Add[something]To[SomeModel] qty_sold:integer

How do you add an index in the migration generation?
- rails generate migration Add[Attribute]To[SomeModel] <attr>:<type>:index
  
How do you add a foreign key in migration generation?
- rails generate migration Add[Attribute]To[SomeModel] <attr>:references
  
Generating a model creates four file types. What are they?
- Model, migration, model test, model fixture

Running `rails generate migration AddQtySoldToProducts qty_sold:integer` will create what single line of code in the #change method?
- add_column :products, :qty_sold, :integer ***
- add_column :qty_sold, :products, :integer
- add_column :products, qty_sold: :integer

On a generation command, what additional line of code is produced in your migration file when running `rails generate migration AddRefNumToProducts ref_num:string:index`?
- add_index :products, :ref_num

What single line of code is produced in your migration's #change method when running `rails generate migration AddStyleToProducts style:references`
- add_reference :products, :style, foreign_key: true

Before Rails version X.y.z, the same migration above would produce what code instead of the newer `add_reference`?
- don't know; need to look up
