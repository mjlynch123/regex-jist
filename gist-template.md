# URL Validation Made Easy with Regex

## Summary

In this tutorial, we'll explore an easy-to-understand regex pattern for validating URLs. You'll learn how to use regular expressions to ensure that URLs have the correct format. We'll break down the regex components and explain their role in the validation process. By the end, you'll have a grasp of URL validation with regex, empowering you to validate URLs efficiently in your projects.

- Regex Pattern: /^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-])/?$/

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
In this section, we will break down the regex pattern /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ and explain each of its components.

### Anchors
The regex pattern starts with two anchors: up array and dollar sign. The up arrow anchor matches the start of the input string, ensuring that the regex pattern starts matching from the beginning of the string. The dollar sign anchor matches the end of the input string, ensuring that the regex pattern matches all the way to the end of the string.

### Quantifiers
Quantifiers specify the number of occurrences of the preceding element. In this regex pattern, the ? quantifier makes the preceding group (https?:\/\/) optional. It allows for URLs with or without the http:// or https:// protocol.

### Grouping Constructs
Grouping constructs ( ) are used to group subpatterns together. In this regex pattern, there are multiple groups:

- (https?:\/\/): This group matches the optional http:// or https:// protocol at the beginning of the URL.
- ([\da-z\.-]+): This group matches the domain name, which can consist of one or more lowercase letters, digits, dots, or hyphens.
- \.([a-z\.]{2,6}): This group matches the top-level domain (TLD), which consists of a dot followed by 2 to 6 lowercase letters or dots.
- ([\/\w \.-]*)*: This group matches optional paths and query parameters. It allows for zero or more occurrences of characters, including forward slashes, word characters, spaces, dots, or hyphens.
- \/?: This matches an optional trailing forward slash at the end of the URL.

### Bracket Expressions
Bracket expressions [ ] are used to define a set of characters that can match at a specific position in the pattern. In this regex pattern, we have two bracket expressions:

- [\da-z\.-]: This matches any digit (\d), lowercase letter (a-z), dot (\.), or hyphen (-).
- [a-z\.]: This matches any lowercase letter (a-z) or dot (\.).

### Character Classes
Character classes are used to match a single character from a specific set or range. In this regex pattern, we have the following character classes:

- \d: This matches any digit from 0 to 9.

### The OR Operator
The OR operator | is used to match either the expression before or after it. In this regex pattern, there is no explicit use of the OR operator.

### Flags
Flags are used to modify the behavior of the regex matching. In this regex pattern, there are no flags specified.

### Character Escapes
Character escapes are used to match special characters or to give them a special meaning. In this regex pattern, we have the following character escapes:

- \/: This matches a forward slash character.

## Author

This tutorial is authored by Martin Lynch. For more information and additional resources, you can visit my GitHub profile [here](https://github.com/mjlynch123)
.
