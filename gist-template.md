# Tutorial: Regular expression (Regex)

Regular Expression, or regex or regexp in short, is extremely and amazingly powerful in searching and manipulating text strings, particularly in processing text files. One line of regex can easily replace several dozen lines of programming codes.It creates rules for email or password to consist of a certain character like lower or upper case character with a symbol and number, those rules can be added using regex. 

## Summary

A regular expression is a pattern describing a certain amount of text. It is matched against a subject string from left to right. Most characters stand for themselves, and match the corresponding characters in the subject text. The simplest form of regular expression is actual literal text.

Example: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

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
Anchors do not match any characters. They match only a particular text position in the string. Meta-character ^ matches at the start of the string/text, and $ matches at the end of the string. Symbol \b matches at a word boundary. E.g. ^B matches only the first B in "B123-B923". \B matches at every position where \b cannot match.. 

### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. The following table lists the quantifiers supported by .NET:
### OR Operator
| Acts like a boolean OR. Matches the expression before or after the |. It can operate within a group, or on a whole expression. The patterns will be tested in order. Just as in java will match either set of characters. It will look for this OR that.
### Character Classes
With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. Simply place the characters you want to match between square brackets. If you want to match an a or an e, use [ae]. You could use this in gr[ae]y to match either gray or grey.

### Flags
A regular expression consists of a pattern and optional flags: g , i , m , u , s , y . Without flags and special symbols

### Grouping and Capturing
Groups group multiple patterns as a whole, and capturing groups provide extra submatch information when using a regular expression pattern to match against a string.

### Bracket Expressions
A bracket expression (an expression enclosed in square brackets, "[]" ) is an RE that shall match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression.
### Greedy and Lazy Match
Greedy and Lazy match are from quantifiers, it is good to understand how the search pattern works

1. Greedy - To find a match, the regular expression engine uses the following algorithm:

2. Lazy - The lazy mode of quantifiers is an opposite to the greedy mode. It means: “repeat minimal number of times”.
 
### Boundaries
When the regexp engine (program module that implements searching for regexps) comes across \b, it checks that the position in the string is a word boundary.

### Back-references
Backreferences match the same text as previously matched by a capturing group. Suppose you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag

### Look-ahead and Look-behind
Sometimes we need to find only those matches for a pattern that are followed or preceded by another pattern.
There’s a special syntax for that, called “lookahead” and “lookbehind”, together referred to as “lookaround”.

## Author

Clarence Bungay

github: https://github.com/dalebungay
