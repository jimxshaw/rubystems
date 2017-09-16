# RubyStems

Supplement and assess your Ruby understanding with multiple choice questions.

Playing off the name of the package management framework [RubyGems](https://rubygems.org/), and keeping with [the technical term](https://en.wikipedia.org/wiki/Multiple_choice#Structure), RubyStems' multiple choice questions will be referred to as **stems**. However, the set of choices known as *alternatives* will simply be called **choices**, and the *key* will be known as **answer**. The **choices** that are not correct will keep with convention and be known as **distractors**.

One very important distinction is that while the entire set of attributes (the question plus the choices) are conventionally known as an *item*, we refer to this collection as the **stem**. What is conventionally known as the *stem* will be for us called the **question**, even when preceded by a statement of relevant information. There will be no fill-in-the-blank statements.

## Example

>Given an array of integers, `arr = [1, 2, 3, 4]`, which of the following statements will *not* return the first element, `1`?
>
>  - `arr[0]`
>  - `arr.at(0)`
>  - `arr.first`
>  - `arr(1)`

## Example Structure

The relevant setup information along with the question is the **question**. The four options are the **choices**. Three of the **choices** are incorrect and therefore **distractors**. And `arr(1)` is correct and therefore the **answer**. The entire example is the **stem**.

## Stem Explanation

My intention in crafting this stem was to expose the lesser known [`#at()` method](https://ruby-doc.org/core-2.4.1/Array.html#method-i-at). I chose not to include another choice like `arr[-4]` because I prefer to limit the choices to four, and given the obscure nature of both `arr[-4]` and `arr.at(0)`, only one ought to be exposed as the learning opportunity. A second, sequential stem could follow to build upon learning the obscure means of accessing array elements.

### Inspiration

[Writing Good Multiple Choice Test Questions](https://cft.vanderbilt.edu/guides-sub-pages/writing-good-multiple-choice-test-questions/)
