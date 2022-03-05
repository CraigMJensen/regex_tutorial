# Regex Tutorial

In this tutorial I will be explaining the regex code for searching for a hexadecimal value. `(#)([A-fa-f0-9]{3}|[A-Fa-f0-9]{6})\b`
This can be used to find any hexadecimal string of 3 or 6 digits long.
A hexadecimal value is a coded value of a color, ex. #fff (yellow) or #DE4A2A (dark orange).

## Summary

The regex code `(#)([A-fa-f0-9]{3}|[A-Fa-f0-9]{6})\b` can be explained one character at a time, read left to right.  
Starting with a group `()` containing a pound sign (hash tag or octothorpe) `#`.
The opening parentheses `(` is the beginning of a second group. The letters and numbers in the square brackets `[A-Fa-f0-9]` indicate
the hexadecimal values (can contain any letter A-F or a-f and any numbers 0-9). The number following in the curly brackets {3},
indicates the amount of values in the hexadecimal number. The pipe character `|` indicates an 'or'. This allows multiple search values
in the grouping. The remaining square brackets and curly brackets are the search values for a six digit hexadecimal number.
Closing the group with an ending parentheses `)`. The `\b` indicates the end of a word boundary.

## Table of Contents

- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Boundaries](#boundaries)

## Regex Components

### Quantifiers

Quantifiers indicate that a preceding value must be matched a certain number of times. ex. `{3} or {6}` In this instance the
preceding value is any value in the square brackets `[A-Fa-f0-9]`.

### OR Operators

The OR Operator or alternation is indicated by the pipe character `|`. This lets multiple cases get evaluated in a single expression.
In the hexadecimal regex it is searching for either `{3}` letter or `|` `{6}` letter strings.

### Character Classes

Character classes are shown in square brackets `[]`. The characters inside the brackets can be predefined, ex. `[A-Za-z0-9]` will use
all letters lowercase and uppercase and all numbers, or you can define your own grouping, ex. `[a-f0-5]` will use lowercase letters
bewteen a and f, and any numbers betweeen 0 and 5.

### Grouping and Capturing

Grouping and capturing is indicated by the parentheses `()`. Groups set a chunk of regex to a separate reference in memory, allowing
you to combine groups together. ex. `(#)([A-Fa-f0-9]{3}|[A-Fa-f0-9]{6})` will use the pound sign with both the 3 value and 6 value
search.

### Boundaries

Boundaries are a type of Anchor `^, $, \b`. They match a position within a string, not a specific character. In this regex we are
using the `\b` anchor for a boundary. This states that the value we are searching will end after either 3 or 6 characters due to the
boundary anchor being placed at the end of the regex expression.

## Author

Craig Jensen is a full stack web developer with a certificate from the UT Coding Bootcamp

- Contact me at: cmjensen82@gmail.com
- Github: https://github.com/craigmjensen/
