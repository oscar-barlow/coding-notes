[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)

---

# Misc. Notes

## Controlling Flow
Ternary conditional expressions are cool. Remember the syntax:

`[boolean to be evaluated] ? [do this if true] : [do this if false]`

Use 'case' instead of endless ifs, elsifs, else. when/then is a nice compact, readable version of endless ifs and elses.

## User Interaction in Ruby
(to be written)

## Parallel Assignment
(to be written)

## Shovel Operator
(to be written)

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
