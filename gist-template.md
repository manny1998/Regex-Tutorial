# Regex Tutorial

Regex expressions are generally used to match character combinations in strings and this can serve multiple purposes. 

## Summary

The regex expression we will be analysing below is  `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`. This regex expression basically means we are looking to match a value which has letters ranging from a-f or numbers ranging from 0-9, with a length of 6 characters or if the first part isnt satisfied then we are looking for a letter from a-f or numbers from 0-9, with a length of 3 characters. 

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

### Anchors
The `^` and `$` characters are anchors. The `^` indicates the start of the string and `$` indicates the end of the string. In our example, `^#` matches to any hex value starting with #.

### Quantifiers
The quantifier used in our regex expression is `{}` also known as a greedy operator. This type of quantifier tells the regex the minimum and maximum number of characters your regex will limit its match to. In our regex expression, `{6}` is limiting the search to exactly 6 characters. Furthermore, the `{3}` it is limiting the search to exactly 3 characters.

### Grouping Constructs

Grouping constructs are usually in the form of `()`, with the `(` representing the start and `)` the end of the group. In our example it starts after the `#?` and ends after `$`. The purpose of grouping constructs being they break up sections of a string to determine if they meet the requirements set out within the regex expression. 

### Bracket Expressions
The square brackets `[]` are used to declare the range of characters we want to match. In our example we have the same square bracket expression used twice with different character limitations.In our regex example,`[a-f0-9]`, means we are looking for a match which has lower case letter ranging from a to f or a number ranging from 0 to 9. 

### Character Classes
Character classes sets the requirements of which set of characters can appear in a string that can be accepted as a match. In our regex example, it was the bracket expressions `[a-f0-9]` which was discussed above. 

### The OR Operator
The `or` operator which is shown in the regex expression as `|`, is used to tell the expression that the value, could be to the right or left of the `|` operator in the expression. It doesn't have to match both sides of the operator either one will qualify a match. In our example, the hex value has to match either `[a-f0-9]{6}` or `[a-f0-9]{3}`. 

### Flags
There are no flags used in the example expression we are using. 
A flag is an optional parameter to a regex that can add filters when  searching. There are several type of flags, with one of the most common being `i` which makes the expression search case insenstivity.

## Author

https://github.com/manny1998 - Manroven Singh
