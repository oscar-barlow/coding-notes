[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)

---

#Ruby Objects
Everything in Ruby is an object. Except for blocks. And even then, some blocks are objects (Procs and lambdas).

## Strings
Ruby knows you want something to be a string when you put `''` or `""` around it. Note, string interpolation doesn't work on strings enclosed in `''`. Typically you use a string to display text or export something out of your program.

If you want to make a multiline string, nest it in three double-quotes, e.g.:

```
"""
This is a
multi-line string
"""
```  

An alternative way to make new lines in strings is to use the newline character: `\n`
`\t` is a tab character.

You can put pretty much whatever you want into a string.

Strings are among the most common objects in Ruby, so it is  worth learning as much about them as you possibly can. At minimum, you should probably memorise what the following methods do, and have an idea of when to use them:

* []
* +
* capitalize
* upcase
* downcase
* length
* include?
* gsub
* slice
* split
* chars

For more, see the [Ruby 2.3.1 String class documentation](http://ruby-doc.org/core-2.3.1/String.html).

## Variables
A way of storing some information under a name that you set. The information is an object, of pretty much any kind (Hash, String, Array, File).

The variable is not itself the object. The variable simply points to the object it contains.

Variable names should be lowercase.

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
A hash is a data structure, used to associated something you want to store (a value) with the tag you want to summon it with (a key).

From LRTHW, this is how they work:

> Let's say you want to find out what the word "Honorificabilitudinitatibus" means. Today you would simply copy-paste that word into a search engine and then find out the answer, and we could say a search engine is like a really huge super complex version of the Oxford English Dictionary (OED). Before search engines what you would do is this:

> 1. Go to your library and get "the dictionary". Let's say it's the OED.
> 2. You know "honorificabilitudinitatibus" starts with the letter 'H' so you look on the side of the book for the little tab that has 'H' on it.
> 3. Then you'd skim the pages until you are close to where "hon" started.
> 4. Then you'd skim a few more pages until you found "honorificabilitudinitatibus" or hit the beginning of the "hp" words and realize this word isn't in the OED.
> 5. Once you found the entry, you'd read the definition to figure out what it means.

> This process is nearly exactly the way a hash works, and you are basically "mapping" the word "honorificabilitudinitatibus" to its definition. A hash in Ruby is just like a dictionary in the real world like the OED.

[(source)](https://learnrubythehardway.org/book/ex39.html)


## Files
(to be written)

---
[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)
