# Matching Hex Values with Regex

## Summary

Matching a Hex Value /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
<br>
This regex is used to match a hexadecimal color value.
<br>
Hexadecimal color values can be represented with a '#' and either 3 or 6 characters
Ex: #cb00eb, #273e31, #fc9, #b58

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)

## Regex Components

### Anchors

Anchors in regex are used to define the positions in the input string where a match should start or end

'^' Is the start of the line anchor

'$' Is the end of the line anchor

Example: `^hello$` will match only if the whole string is "hello"

### Quantifiers

Quantifiers are used to specificy how many times a character or group should occur in an input

'{6}' Means should match 6 times

'{3}' Means should match 3 times

Example: `[0-9]{1,5}` would match 1 to 5 consecutive digits

### OR Operator

The OR operator - the pipe symbol '|' is used to let you specify other patterns

(pattern1|pattern2)

Example: `(tomato|potato)` would match "tomato" OR "potato"

### Character Classes

Character classes are used to define a specific set of characters that can match in a specific position of the input

`[a-f0-9]` Would match any character thats in the range of a-f or from 0-9

Example: `[A-Z]` would match any uppercase letters

### Grouping and Capturing

Grouping and capturing is represented with `()` parenthesis. Used to grab specific parts of the regex

`(pattern)`

Example: `(\d{3})-(\d{3})` Would match to a group of 3 digits with a dash in between them

### Bracket Expressions

Bracket expressions are defined with [] square brackets and are used to set a character class

`[a-f0-9]` Would match any characters from range of a-f or numbers from 0-9

Example: `[abcd]` would match any a, b, c, d characters

### Greedy and Lazy Match

Greedy and Lazy match in regex are used to determine if something matches either the maxiumum or the minimum number of characters that are defined

`*?` is considered lazy match which would match only the minimum number of characters

`*` is considered a greedy match which would match the maximum number of characters

Example: `h.*o` taking the input of 'helloooo' would return a greedy match of 'helloooo'
and a lazy match `h.*?` taking the same input would match with 'hello'

### Boundaries

Boundaries of a regex are the starts and ends of a regex expression

The anchors `^` and `$` are used to represent the start and end of a line or the boundaries

^start

$end

Example: `^\d{4}$` would match a 4 digit number at the start and at the end of a line

## Author

https://github.com/joshuawongg
