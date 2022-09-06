# Regex Tutorial


## Summary

REGEX means regular expression. They are useful for useful in extracting information from any text by searching for one or more matches of a specific search pattern (i.e. a specific sequence of ASCII or unicode characters).


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
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
Anchors expressions are ^ to start and $ at the end

### Quantifiers
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
The expression has a + to show there is another sequence to be matched as a greedy quantifier. {2,6} are another greedy quantifier that specify the input should be a minimum of 2 characters and maximum of 6 characters.

### OR Operator
"OR" syntax is denoted with a certifcal line "|"
In HTML, CSS, javascript the corresponding RegEx would look like: html|css|javascript(script).

### Character Classes
It allows you to match any symbol for a certain character set. Most common character classes are:
\d-match it with a digit or character from 0-9. \s- match a whitespace symbol such as space, tab (/t). A newline (/n), ect. \w- W stands for word character. It matches it matches the ASC|| character [A-Za-z0-9] including Latin alphabets, digits, and the underscore(_).

### Flags
Flags are optional paramaters that we can add a plain expression to make it search a different way. Each glag is denoted by an alphabetical character, it serves different purposes in modifying the expressions seaching behavior.
i Ignore casing makes the expression search case insensitively. g Global makes the expression search for all occurrences. s Dot all makes the wild character match newlines as well. m Multiline makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string. y sticky makes the expression start its search from the index indicated  in last index property. u unicode makes the expression assume the individual characters as code points. It matches a 32-bit characters as well.

### Grouping and Capturing
Grouping is done with the round brackets or parentheses and allows to group a certain part of the regular expression together. /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

This expression would be split like so:
1st - ([a-z0-9_.-]+)
2nd - ([\da-z.-]+)
3rd - ([a-z.]{2,6})

### Bracket Expressions
Brackets indicate a set of characters to match. you will often see ranges of the alphabet or numerals. [A-Za-z] [0-9].
([a-z0-9_.-]+)
This grouping it will look for anything a-z or 0-9

### Greedy and Lazy Match
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
This example we have only used greedy quantifiers + and {}, meaning that it will allow the match to expand as long as it neess to go. If these quantifiers were lazy quantifiers, they would appear as +? or {}?, this will direct the system to make the shortest match.

### Boundaries
The (\b) is an anchor like the caret (^) and the dollar sign ($) it matches a position that is called a "word boundary". the word boundary match is zero-length.
console.log('hello, js!'.match(/\bjs\b/)):
The output would be ["js"]

### Back-references
A back-reference in a regular expression indetifies a previously matched group and looks for exaclty the same text again. They are specified with a backslash and a single digit. \1

### Look-ahead and Look-behind
n some cases we need to find only those matches for a pattern that are followed or preceeded by another pattern the syntax for that is called look-ahead and look-behind.

Look-ahead uses syntax that looks like this: X(?=Y). This means "look for X, but match only if followed by Y.

Look-behind is similar bit looks behind to match a pattern only if there is something before it. the syntax looks like: (?<=Y)X. Matches x but only if Y is before it.
## Author
Madison Mulligan- https://github.com/maddyrae9