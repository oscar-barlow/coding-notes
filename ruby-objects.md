[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)

---

#Ruby Objects
Everything in Ruby is an object. Except for blocks. And even then, some blocks are objects (Procs and lambdas).

## Strings
(to be written)

## Variables
(to be written)

## Methods
(to be written)	

## Booleans
(to be written)

## Arrays
(to be written)

## Controlling Flow
(to be written)

## Symbols

### Why it is generally better for performance to use symbols as keys in hashes, rather than strings?
As far as a computer is concerned, a string is a list of numbers. A symbol, on the other hand, is only one number.

When you go look something up in a hash, ruby does complicated magic maths (hashing). If you give ruby a string to look something up in a hash with, ruby has to use magic maths on the whole list of numbers you've given it to produced a single magic-hashed number, which it then goes and checks against a list of magic-hashed such numbers stored in your hash*.

The magic-hashed number is a unique number, the result of a mathematical equation, distinct from the id of an object.

In contrast, a symbol is represented in your computer by one number, not a list. Thus, when you give ruby a symbol to go and look something up with, ruby only has to apply magic maths to that single number which it can then go and look up against the magic-hashed numbers. This is faster.

Basically, because computers do maths and speak numbers, it's faster to make ruby do less maths

*when you add something to a hash, not only are the key and value stored, also magic hashing maths is applied to at least the key to produce a singled magic-hashed number for it.

## Hashes
(to be written)

## Blocks
(to be written)

---
[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)
