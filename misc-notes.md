[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)

---

# Misc. Notes

## Controlling Flow
Get ruby to logically evaluate a statement. If it evaluates to true, execute a given block of code. If false, execute a different block. You can use `elsif` to set additional conditions, but it's usually a bit clunky.

Ternary conditional expressions are cool. Remember the syntax:

`[boolean to be evaluated] ? [do this if true] : [do this if false]`

Use `case` instead of endless ifs, elsifs, else. `when`..`then` is a nice compact, readable version of endless ifs and elses.

## Booleans
When a statement is logically evaluated in Ruby, it returns either `true` or `false`. These are Booleans.

By default, everything in Ruby is `true`. Only `nil` and `false` are false.

## User Interaction in Ruby
`gets` takes user input from the command line. By default, it adds a newline at the end. By using `.chomp` at the same time, you remove the last character of the input - in the case of `gets` this means removing the newline.

`gets.chomp` doesn't play nicely with `ARGV` (in which you pass arguments from the command line into the script) and `$stdin.gets.chomp` should be used instead.

I know that's a global variable, but I have no idea what the `stdin` part does.

## Parallel Assignment
This is where you assign values to multiple variables at once. You saw this in LRTHW with `ARGV`:

```
$ script.rb var1 var2 var3
```
Assigns the three arguments after the script name to, in your script...

 ```
first, second, third = ARGV
 ```

You can use this in other contexts than `ARGV` though. The [Ruby Pills](https://github.com/makersacademy/pre_course/blob/master/pills/parallel_assignment.md) give the example:

```
age = player[:age]
name = player[:name]
```

Which can be refactored as `age, name = player[:age], player[:name]`.

## Shovel Operator
Pushes something into an array.

## String Interpolation
Use `#{var}` to 'interpolate' the value assigned to a variable into a string.
If you want to apply the same formatting to multiple values, use `%{var1 var2 var3}`

String interpolation (`#{var}`) doesn't work on strings enclosed in single quotes.

## Classes
The canonical form of an object.

## Modules
Modules are like classes but they can't create instances. They're only used for storing things (constants).

## Mixins
When you use a module to add information to a class.

## ARGV
Stands for 'argument variable'. If you supply a ruby script with an argument on the command line (or any other way, I guess?) then `ARGV` passes those arguments into the script.

Multiple arguments may be passed, as long as you 'unpack' them in the script, i.e.

`first, second, third = ARGV`

Will pass 3 arguments from the command line, in order, to variables `first`, `second`, and `third`. `ARGV` doesn't play nicely with `gets.chomp` so you have to use `$stdin.gets.chomp` instead.

---
[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)
