# Title (Matching an Email Regex Tutorial)

In this tutorial, we will be taking a look into what Regex (regular expressions) are and how they work. We are going to use the expression for validating emails which is useful in applications like Node (inquirer) or MongoDB.

## Summary

A regular expression is a sequence of characters that defines a search pattern. It is most commonly used to find a search pattern in a string but can also be used to find/replace characters with a string or validate an input. 
This tutorial will go walk through the components of this expressions `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` and how it applies to matching and validating emails. 


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

`/^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$/`

The anchors as they are show in the highlighted formate are used to start and end a string or an expression. 
In this regex expression for `/^` is used, which indicates the beginning of the string and `$/` is used to indicate the ending of the string. Sometimes `(m)`, or multiline is not enabled, so the regex will end at `$/`.

### Quantifiers

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

Quantifiers are used communicate how many characters are expected. Quantifiers by default will match as many characters as possible. If ",+,?,{}" are characters found in the expression they are considered quantifiers. 
Quantifiers in this regex includes the `+` operator, which will connect the users email name + email service + `.com`. Another quantifier for this regex includes `{2,6}`, which will allow a match range of 2-6 characters for the character set of `[a-z\.]`.

### Character Classes

/^([a-z0-9_\.-]+)@([`\d`a-z\.-]+)\.([a-z\.]{2,6})$/

Character classes are components within our regular expression that tells us what type of characters to expect. 
Our character expressions are found in brackets `[]`. 
Character classes can only match one out of several specific characters. The character class in this expression is \d, which matches a single digit from 0-9. It will only match a single digit such as any digit 1 though 9 but not double digits such as 11. There is also `.` which can match with any character. 


### Grouping and Capturing

/^`([a-z0-9_\.-]+)@([\da-z\.-]+)`\.`([a-z\.]{2,6})`$/

Grouping and capturing unifies a pattern or string so that it can match in a complete block.
Captured groups are found between parentheses `()`. The first capturing group in this expression is `([a-z0-9_\.-]+)` and matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. The last capture group is `([a-z\.]{2,6})` to capture the .com.

### Bracket Expressions

/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

Bracket expressions as the name suggests are found in between our brackets `[]` and are signified by the beginning of a character class or quantifier statement. Email validation for our expression includes the character sets of `[a-z0-9_\.-]`, `[\da-z\.-]`, `[a-z\.]` which is matching any letter a-z and is case sensitive. It also matches a character 0-9 and matches the characters "_" , "-" , and ".".

### Greedy and Lazy Match

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

A greedy match tries to match an element as many times as possible. A lazy match tries to match an element as few times as possible. This Regrex includes greedy matches. The `+` quantifier is one such match and will match as many times as possible. Another greedy Quantifier used in this regex is `{}` when matching `{2,6}` for the last capture group.

## Author

Alexander Kenney

Alexander Kenney is a junior developer working towards the end of his coding bootcamp through UPenn in Philadelphia. 

Feel free to checkout his github repo and all his previous projects here: https://github.com/Aken00 

