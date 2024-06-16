# Title (replace with your title)

This tutorial aims to explain the regular expression used to validate email addresses. By breaking down each part of the expression we can understand how it functions to ensure that a user enters a valid email address.

## Summary

The regex we will be going over is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This regex, as mentioned above, is used to verify that user input is a valid email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)


## Regex Components

### Anchors

In our regex, the `^` and `$` are anchors. The `^` asserts the start of a line, while the `$` dictates the end of a line. The pattern defined by the regex has to match the entire string, not just a part of it.

Example: `^abc$` will match the string of "abc" but wont match "abcd" or "eabc".

### Quantifiers

The `+` symbol is a quantifier. In this regex it is used after character classes. It is used to mean "one or more" of the preceding elements. 

Example: `[a-z0-9_\.-]+` matches one or more of any lowercase letter, digit, underscore, dot or hyphen.

### Character Classes

Character classes are defined by `[]`. In this regex, `[a-z0-9/-.]` is a character class that matches any lowercase letter, digit, underscore, dot or hyphen.

Example: `[abc]` would match any single character that is either "a", "b" or "c".


### Grouping and Capturing

Parentheses `()` are used for grouping and capturing. Parts of the regex enclosed in parenthesis are considered a single unit. In this regex `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, and `([a-z\.]{2,6})` are groups. The `@` symbol and the `.` are not part of these groups so they have to appear literally in the string.

Example: `(abc)+` would match any of the following "abc", "abcabc", "abcabcabc", etc., but it would not match "ababc".

## Author

This tutorial was made by Jonathan Fajardo (https://github.com/Jfajardo18)
