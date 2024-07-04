Regex Tutorial: Understanding HTML Tag Matching
Introduction
As a web development student, I have developed this tutorial to explain the specifics of regex so that we can understand the search pattern it defines.

Summary
A Regex, or regular expression, is a sequence of characters that define a search pattern. These patterns are used in string-searching algorithms for "find" or "find and replace" operations on strings. They are also used for input validations. Regex is a technique commonly developed in theoretical computer science.

In this tutorial, we will look at a regex pattern that matches HTML tags.

Example Regex: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
The following content will explain what each section of this regex does and more.

Table of Contents
Anchors
Quantifiers
OR Operator
Character Classes
Flags
Grouping and Capturing
Bracket Expressions
Greedy and Lazy Match
Boundaries
Back-references
Look-ahead and Look-behind
Author
Sources and References
Regex Components
Anchors
^ and $

^: Matches the beginning of the string.
$: Matches the end of the string.
These anchors ensure that the entire string must match the pattern from start to end.

\b and \B

\b: Matches a word boundary position between a word character and a non-word character.
\B: Matches any position that is not a word boundary.
Quantifiers
Quantifiers indicate that the preceding token must be matched a certain number of times.

*: Matches 0 or more of the preceding token.
+: Matches 1 or more of the preceding token.
?: Matches 0 or 1 of the preceding token, effectively making it optional. Also makes the preceding quantifier lazy, causing it to match as few characters as possible.
{n}: Matches exactly n occurrences of the preceding token.
{n,}: Matches n or more occurrences.
{n,m}: Matches between n and m occurrences.
OR Operator
|: Acts like a boolean OR, matching the expression before or after the |.
Character Classes
Character classes match a character from a specific set.

[ABC]: Matches any character in the set.
[^ABC]: Matches any character not in the set.
[A-Z]: Matches any character in the range.
.: Matches any character except line breaks.
\w: Matches any word character (alphanumeric & underscore).
\W: Matches any non-word character.
\d: Matches any digit character (0-9).
\D: Matches any non-digit character.
Flags
Flags change how the expression is interpreted.

i: Ignore case.
g: Global search.
m: Multiline mode.
u: Unicode.
y: Sticky mode.
s: Dotall mode, allowing . to match newline characters.
Grouping and Capturing
(ABC): Capturing group.
(?<name>ABC): Named capturing group.
\1: Backreference to the first capturing group.
(?:ABC): Non-capturing group.
Bracket Expressions
A bracket expression matches a single character.

[a-z]: Matches any character in the range.
[^a-z]: Matches any character not in the range.
Greedy and Lazy Match
Greedy: Matches the longest possible string.
Lazy: Matches the shortest possible string by appending ? to the quantifier.
Boundaries
\b: Matches a word boundary.
\B: Matches a non-word boundary.
Back-references
Backreferences match the same text as previously matched by a capturing group.

Example: <([A-Z][0-9]*)\b[^>]*>.*?</\1>

Look-ahead and Look-behind
(?=ABC): Positive lookahead.
(?!ABC): Negative lookahead.
(?<=ABC): Positive lookbehind.
(?<!ABC): Negative lookbehind.
Author
Christopher Even: UT coding student.

Sources and References
Regexr
Backreferences
Word Boundaries
My GitHub:https://github.com/ortzfrancisco