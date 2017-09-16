# Generating a Controller in Rails

> [Rails Guide](http://guides.rubyonrails.org/command_line.html#rails-generate): Using generators will save you a large amount of time by writing **boilerplate code**, code that is necessary for the app to work.
>
> From the command line, the first part of the command is `rails generate controller` followed by the controller name, and then any controller actions. Which of the following demonstrates the conventional way of generating a subjects controller with index and show actions?
>
> `rails generate controller ...`
> - `Subjects index show`
>   - Correct! That's the capitalized and plural controller name, then the actions.
> - `SubjectsController index show`
>   - No need to append "Controller" to the controller portion
> - `Subjects, action: :index, action: :show`
>   - The controller action doesn't use hash notation
> - `Subjects index:action show:action`
>   - Generating a model can use the attribute[:type] notation, e.g. `title:string` means "title of type string". Generating a controller does not use this "of type" notation.

## Providing Context

The nested comments would be shown perhaps as a `flash[:notice]` upon selection.

## Earning Points

Once we have users who can earn points, we can assign partial credit based on subsequent attempts. The total score would be based on a collection of stems.
