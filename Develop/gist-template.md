# Matching an Email - Regex Tutorial

Matching an Email 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Summary

Regex is useful for matching text. It is a testing tool for matching (pattern matching) for certain strings. Pieces or sub portions of a matched string with the intent of extraction

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

From : 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

For the component matching behavior of an email address, we can break up the expression into its identifying components 

These components are required for establishing the regular expression: 
- `/` -> the forward slash must match the beginning and end of the expression string 



### Anchors

- `$` -> Is required to match at the end of the string (End of string)
- `^` -> The given input string has to match the start of this expression 


### Quantifiers

`([a-z\.]{2,6})`

The quantifiers are required for the top-level domain, which must be between two and six characters and consist of only lowercase letters. The brackets denote that you need 2 to 6 of the bound expression. 


### Grouping Constructs

1. `([a-z0-9_\.-]+)`  - Matches the username of the email
2. `([\da-z\.-]+)`  - Matches the subdomain
3. `([a-z\.]{2,6})` - Matches the top-level domain

Grouping constructs are anything within parentheses. 


### Bracket Expressions

1. `[a-z0-9_\.-]`  - Username consists of lowercase letters, underscore, dot, or dash
2. `[\da-z\.-]`  - subdomain, consists of any digit (\d), any lowercase letter, dot or dash
3. `[a-z\.]` - top-level domain, consists of any lowercase letter or dot 

### Character Classes

- `\d`  - used by matching subdomain, can contain any digit (\d)

### The OR Operator (Alternation)

Not used in this example however, 

- (abc):(xyz) = (a|b|c):(x|y|z)
    - Can be used for further matching between alternate acceptable patterns

### Flags

Not used in this example, however, 

- After the ending `/`, you can add `g` (global search), `i`(case-sensitive search), or `m`(mult-line search) as optional flags

### Character Escapes

Character escapes treat the `.` in a literal context, rather than match any character 

## Author

![Github Link](github.com/BrandtDavidson)
