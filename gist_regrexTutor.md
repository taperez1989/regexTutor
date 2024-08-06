# regexTutor

Regex refer to encoded text strings designed to match patterns in other strings. Regular expressions are particularly helpful when you need to find a string of characters that matches a certain type of pattern. A common usage for regex is email validation

## Summary

A regex email validation can typically be done with one or two lines of code and can be modified to handle a wide range of different parameters. A basic email validation regex could be as followed

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{3,9})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
"^" and "$" they match a position before, after, or between characters. They can be used to “anchor” the regex match at a certain position of the algorithm. For instance the caret "^" matches the position before the first character in the string. Example of this could be "^a" to "abc" ould would mean that it matches to the 'a'. we would want to use the caret in terms of email validation just so we can make sure we start the search with a character we expect to be in the email.

### Quantifiers
Quantifiers specify the number of characters to match. This is typically located to the right of the expression and look like so: {2,6})$/. youll see this when we are looking for a ".com", ".net" etc. when we are only looking for a period that contains only 2-6 letters long.

### OR Operator
 The OR "|" Operator tells the regex to match the pattern either before it or after it. an example of this would be .(com|net)$/

### Character Classes
\d - Digit character class macthes any digit character [0-9]. \w - Word character class matches any alphanumerical character and underscore. which would include both upper and lowercase characters  [a-zA-Z0-9_].
\s - Whitespace character class matches any whitespace character which includes line breaks, tabs and spaces.

### Flags
Regular expressions may have flags that affect the search.
g(global) looks for all matches, without it – only the first match is returned. i(insensitive) search is case-insensitive: no difference between A and a.

### Grouping and Capturing
Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses. For example, the regular expression (fish) creates a single group containing the letters "f" "i" "s" "h". The portion of the input string that matches the capturing group will be saved in memory for later.
Grouping is a feature of regex that can simplify a complex pattern. You can use grouping to match repeated sequences of characters, such as phone numbers or email addresses. (abc) creates a group that matches the exact sequence "abc".

### Bracket Expressions

Bracket expressions "[]" match one character out of a set of characters, just like regular character classes. Numbers and other characters can be include in your bracked expression. "[abc]" matches a string that has either an a or a b or a c -> is the same as a|b|c.

### Greedy and Lazy Match
'Greedy' means match longest possible string.

'Lazy' means match shortest possible string

### Boundaries
"boundaries" usually refer to the rules or limits set to determine whether an email address is considered valid or invalid.

### Back-references
A backreference is a way to match the same text as previously matched by a capturing group. apturing groups count from 1, so the first capturing group's result can be referenced with \1, the second with \2, and so on. ex from earlier would be the (fish) capture in the previous section.

### Look-ahead and Look-behind
Lookahead assertions check if a pattern is followed by another pattern, but they do not consume characters in the input string. Look-ahead ((?=...)):  Asserts that what follows the current position in the string matches the specified pattern. Lookbehind assertions check if a pattern is preceded by another pattern, but they do not consume characters in the input string. Look-behind ((?<=...)):  Asserts that what precedes the current position in the string matches the specified pattern.

## Author

github: https://github.com/taperez1989/regexTutor.git