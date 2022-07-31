# RegEx for Valdating an Email:

This gist will explain a regex used for validating an email address.

## Summary:

This regex explains how /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ is used as email varification. This regular expression is case sensitive and won't validate if there is whitespace after an email address.

## Table of Contents:
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [OR Operator](#or-operator)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)
- [About Me](#about-me)

## Expression Componets:

### Anchors:

Start of String (^) End of String ($)

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 

The ^ and $ are anchors with the ^ matching the beginning of the text and the $ matching the end. Together these are used to test if a string completely matches a pattern. For example, to check if the users input is in the correct format for email addresses, the anchors (^,$)  are tests and have zero width. This is important to ensure the pattern knows where to start and stop the search.

### Quantifiers +, *, ? and {n}:
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 

"{n}" A number in curly braces is the simplest quantifier: {n}. {4,8} will match between 4 and 8 of the preceding token .

“+” = one or more and the same as {1,}. In this snippet the + joins three groups. 
<br>
"*" = zero or more and the same as {0,}. The character can repeat any times or not be there at all. 
<br>
"?" = zero or one and the  same as {0,1}. Making the symbol optional.

### Character Classes \d \s \w .:

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 
<br>
\d = “digit” (ex=a number)
<br>
\s =“space” (ex=a space)
<br>
\w = “word” (ex=a word)
<br>
A character class is a notation that matches any symbol from a particular set. \d is the only example and indicates a "digit"

#### Inverse Classes \D \S \W

\D = non-digit (ex=a letter)
<br>
\S = non-space (ex=a letter)
<br>
\W = non-word characters (ex=a non-latin letter or a space)
<br>
Inverse classes are not utilized in this code snippet.

### Alternation/ OR operator:
Alternation is a term in an regex that essentially means ‘OR’. It is signified with ‘|’ and is not used in the code snippet.

### Flags:
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 
<br>
Flags are typically used to express special characters (symbols, punctuation, Hex_Digit, etc.)
Flags are expressed in this snippet and are only used to  "escape" so that the following character(s) can be expressed as they are meant to, not as a function/wildcard. The "." in each grouping needed to present as a literal as well as the "-" in the first two groupings. 

### Grouping and Capturing:

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 

#### ( ) Parentheses:
Group together a part of the regex, so that the quantifier will apply to it as a whole. A part of a pattern can be encased in parentheses (...). This is referred to as “capturing group”. 

##### Grouping 1:
([a-z0-9_.-]+) matches a range of “a” to "z" case sensitive matches a range of “0” to "9" matches a "_" character . matches a "." character matches a "-" character

##### Grouping 2:

([\da-z.-]+) matches a digit character (0-9) matches any lower case character "a" to "z" . Escaped character matches any  "." "-" matches a "-" character.

##### Grouping 3:
([a-z.]{2,6}) Matches a range of “a” to "z" case sensitive . Escaped character matches a "."

### Bracket Expressions:
[ ] A bracket expression in square brackets is a regular expression that matches a single character/ collating element. Square brackets indicate character classes, which matches characters in a character set. Each group in this regular expression contains a bracket to match a series of characters therefore allowing a sting.

### Greedy and Lazy Match:

#### Greedy:
/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ 
The regular expression engine will try to repeat the quantifier as many times as is can by default. \d+ consumes all possible digits. When it is no longer possible to consume more (no more digits or string end), it will continue to match the rest of a pattern. If there is no match, it decreases the number of repetitions and tries again. In this snippet, Greedy Match is used in the second group to gather any pattern of numbers and lower case letters.

#### Lazy:
While not utilized in this snippet, it is enabled  by the question mark after the quantifier. The regular expression engine will try to match the rest of the pattern before each repetition of the quantifier.

### Boundaries:
Not utilized in this snippet but like  ^ and $ a word boundary \b is a test.

### Back-references:
Not utilized in this snippet but we can use the contents of capturing groups (...) in the result, replacement string, and in the pattern itself.

### Look-ahead and Look-behind:
Not utilized in this snippet but we can use this to find only those matches for a pattern that are followed or preceded by another pattern.

### About Me:
Hi, I'm Justice! I am currently enrolled in the MSU coding bootcamp and am a fulltime employee for an awesome company. I hope to transition into a developer role within my current company once I complete this program.
#### GitHub Link: https://github.com/JPage96

