In your Rails application you've discovered the need to have a one-to-one association between your Student and IdCard model. Which of the following definitions is correct?

```ruby
class Student < ApplicationRecord

- a. `has_one :id_card`
- b. `has_many :id_cards`
- c. `has_a :id_card`
- d. `belongs_to :id_card`

end
```

What should the corresponding definition be for the IdCard model?

```ruby
class IdCard < ApplicationRecord

- a. `has_one :student`
- b. `has_many :students`
- c. `scope :student`
- d. `belongs_to :student`

end
```
