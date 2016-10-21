[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)

---
# Ruby Methods

## Definition

What Ruby calls a method, many other languages call a function. Functions do 3 things:

> 1. They name pieces of code the way variables name strings and numbers.
> 2. They take arguments the way your scripts take ARGV.
> 3. Using 1 and 2 they let you make your own "mini-scripts" or "tiny commands."

[(source)](https://learnrubythehardway.org/book/ex18.html))

You write methods so that you don't have to keep on writing the same code over and over again.

Running, using or calling a function/method all means the same thing.

## Arguments/Parameters
Are the values you give to a method for it to work on. Theoretically you could define a method that takes tons and tons of arguments.

Practically speaking, a method that takes more than 5 arguments is probably going to be a pain to use.

## Can a given method be used on a given object?
`[variable].respond_to?(:methodname)`

Checks if a given method can be used on a given type of object, assigned to a variable. OMG THAT IS MEGA USEFUL!

## Blocks
A block is just a piece of code between `do`..`end`. It's not an object on its own, but it can be passed to methods like `.each` and `.select`. [source](https://www.codecademy.com/learn/ruby).

Blocks can be written multiple different ways. I generally do them more verbose if I'm working them out, or if the block is complex and I want to make it clear to a later reader what's going on.

## Procs
A proc is just a saved block we can use over and over again.

## Lambdas
A lambda is like a proc, but it cares about the number of arguments gets and returns to its calling method rather than returning straight away.

## Recursion
Recursion is where you call a method on itself. It's super clever. For more, see [Chris Pine's EnglishNubmer program](https://pine.fm/LearnToProgram/chap_08.html).

## Gems
(to be written)

---
[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)
