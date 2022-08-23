# REGEX EMAIL VALIDATION TUTORIAL
In this tutorial, I will be explaining the email validation regular expression, the pieces of the expression, and how they work together to check for strings of characters that fit the criteria.

## Summary

I have chosen the regular expression that checks for email adresses. The expression itself is as follows: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
The rest of the tutorial is broken into pieces, which I will walk you through step by step, explaining to the best of my ability.

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
A regular expression is a literal that searches for strings of characters that match a certain criteria. The regex must be wrapped in / characters, and everything that comes between are the components of the expression that specificy what will be searched.

### Anchors
Anchor metacharacters specifiy position in a searched block of text. ^ specifies a string that begins with the character that follows it, and $ specifies a string that ends with the character that precedes it.
Within the context of the find email address expression, the carat at the beginning means that we are searching for a string that begins with the criteria contained in the following square brackets. The dollar sign at the end is specifiying what the string will end with.

### Quantifiers
Quantifiers are metacharacters that modify the criteria of the previous metacharacter. for instance, ? means 0 or 1, effectly making it an optional part of the search. * means 0 or more, basically checking for a characters existance without a specific quantity. A search of .* means any character at all will be selected.
In the email example, each + indicates that the number of characters in the specified part of the string is irrelevant.

### OR Operator
| is the OR operator in regex. You use it when you want to apply or logic outside of a bracket expression. 

### Character Classes
Character classes define a set of characters.
Literal characters are used to find a specific character, literally. You can put them in brackets to indicate that more than one character can fulfill the search. For example, [abc]. Any of those three letters will be found in the search. 
Metacharacters do not indicate a specific character. They are used to find single characters based on criteria. For example, \w will find any letters uppercase or lowercase, and any digits 1-9. That means anything other than white space will be selected in a \w search. . will match any character except for the newline character, \m

### Flags
Flags are the one component of a regular expression that go outside the containing slashes. g indicates that it is a global search, that the regex should bet tested against all possible matches. i indicates that the search is case insensitive. m meeans that a multi-line input string should be treated as multiple lines.

### Grouping and Capturing
Regular expressions can be split into groups using parentheses. Grouping allows you to refer to those specific parts. Group 0 is the global scope of the expression, and additional groups are numbered according to their order in the expression starting from 1. When you group part of an expression, the part of the search that that grouped section returns is "captured", and can be replaced using $

### Bracket Expressions
The characters contained within square brackets represent a range of characters we want to match.

### Greedy and Lazy Match
Greedy and lazy matching has to do with repetition operators. Greedy is when an operator is going to try and match as many things as it possibly can. When the criteria of the search need to be more specific to return only what is needed. Lazy is when an operator is going to try and match as few things as possible. Commonly it's when the ? operator is used improperly, causing the first part of the criteria to be satisfied immediately, making the compiler fail continually trying to move onto the next step too soon.

### Boundaries
/b is the word boundry metacharacter, meaning if you search \b\w{5}\b, you will be returned words that contain only five letters. It creates boundries for the search.

### Back-references
After you capture a group from an expression, you can reference it with it's corresponding number.

### Look-ahead and Look-behind
Look-ahead and look-behind are similar to the start and end of line anchors I explained earlier. It lets you refer to the found value of a previous or following section of the expression

## Author

My name is Connor Carciofini! I can be reached at [GITHUB]()
