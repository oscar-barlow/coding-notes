[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)

---

#Ruby Objects
Everything in Ruby is an object. Except for blocks. And even then, some blocks are objects (Procs and lambdas).

## Strings
Ruby knows you want something to be a string when you put `''` or `""` around it. Typically you use a string to display text or export something out of your program.

If you want to make a multiline string, nest it in three double-quotes, e.g.:

```
"""
This is a
multi-line string
"""
```  

An alternative way to make new lines in strings is to use the newline character: `\n`
`\t` is a tab character.

## Variables
(to be written)

## Methods
(to be written)

## Booleans
(to be written)

## Arrays
The difference between `.collect` and `.select`:

* Collect is simpler in that it returns the value of running a block on each element of an array into a new array
* Select runs the each element of an array through a block and (usually this is how you would write it) and returns the elements of the original array that conform to the criteria you've set out in your block

`.inject` sounds like a really useful method for an array, I wish I knew how it worked!
`.join()` compresses an array into a string and is super useful.

You can use array methods on any collection, not just arrays. e.g. ranges (`1..10`) or files, which ruby treats as a collection of lines.

## Symbols

### Why it is generally better for performance to use symbols as keys in hashes, rather than strings?
As far as a computer is concerned, a string is a list of numbers. A symbol, on the other hand, is only one number.

When you go look something up in a hash, ruby does complicated magic maths (hashing). If you give ruby a string to look something up in a hash with, ruby has to use magic maths on the whole list of numbers you've given it to produced a single magic-hashed number, which it then goes and checks against a list of magic-hashed such numbers stored in your hash*.

The magic-hashed number is a unique number, the result of a mathematical equation, distinct from the id of an object.

In contrast, a symbol is represented in your computer by one number, not a list. Thus, when you give ruby a symbol to go and look something up with, ruby only has to apply magic maths to that single number which it can then go and look up against the magic-hashed numbers. This is faster.

Basically, because computers do maths and speak numbers, it's faster to make ruby do less maths

\*when you add something to a hash, not only are the key and value stored, also magic hashing maths is applied to at least the key to produce a singled magic-hashed number for it.

## Hashes
(to be written)

## Files
(to be written)

---
[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)
