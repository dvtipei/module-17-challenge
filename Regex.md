# Module 17 Challenge

Regex Tutorial by Denis Voia-Tipei

## Summary

     This tutorial will dive into the Regex Email expression of `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,5})$/`.  This expression is able to match email address formats needed for verification.  The formatting is what we have come to expect of all email address; examples of this format would be first.lastName123@email.com, anyword@domain.com, and so on.  The following sections of this piece will examine the various components of a Regular Expression and how they are used.  


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
^ - Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled. This matches a position, not a character.
$ - Matches the end of the string, or the end of a line if the multiline flag (m) is enabled. This matches a position, not a character.

### Quantifiers
{2,6}
### OR Operator

### Character Classes
^  Beginning.  Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled. This matches a position, not a character.
(  Capturing Group 1.  Groups multiple tokens together and creates a capture group for extracting a substring or using a back reference.
[  Character set. Match any character in the set.
a-z  Range.  Matches a character having a character code between the two specified characters inclusive. Case Sensitive.
0-9  Range.  Matches a character in the range "0" to "9". Case sensitive.
_  Character.  Matches a "_" character (char code 95).
\.  Escaped character. Matches a "." character (char code 46).
-  Character.  Matches a "-" character (char code 45).
]
+  Quantifier.  Match 1 or more of the preceding tokens.
)
@  Character.  Matches a "@" character (char code 64).
(  Capturing Group #2.  Groups multiple tokens together and creates a capture group for extracting a substring or using a back reference.
[  Character set. Match any character in the set.
\d  Digit. Matches and digit character (0-9).
a-z  Range. Matches a character in the range "a" to "z" (char code 97 to 122). Case sensitive.
\.  Escaped character.  Matches a "." character (char code 46).
-  Character. Matches a "-" character (char code 45).
]
+  Quantifier.  Match 1 or more of the preceding token.
)
\.  Escaped character.  Matches a "." character (char code 46).
(  Capturing group #3.  Groups multiple tokens together and creates a capture group for extracting a substring or using a back reference.
[  Character set. Match any character in the set.
a-z  Range. Matches a character in the range "a" to "z" (char code 97 to 122). Case sensitive.
\.  Escaped character.  Matches a "." character (char code 46).
]
{2,6} Quantifier.  Match between 2 and 6 of the preceding token.
)
$  End.  Matches the end of the string , or the end of a line if the multiline flag (m) is enabled.

### Flags
Expression flags change how the expression is interpreted. Flags follow the closing forward slash of the expression.

### Grouping and Capturing
Groups multiple tokens together and creates a capture group for extracting a substring or using a back reference.

### Bracket Expressions
[] Any characters specified between the opening and closing brackets will be searched | ````[C]a[tr]```` means any matching strings that have ````C```` followed by an ````a```` then a ````t```` or a ````r```` like : ````Car```` or ````Cat````|````[a-z0-9_\.-]```` means any matching with ````a-z0-9_\.-````
[-] Specifies any matching within the range of characters (character on the left side of the hyphen ````-```` is the start of the range and the character on the right side of the hyphen specifies the end of the range) | ````[a-z]```` means any matching character between letter ````a```` in small caps and ````z```` in small caps (including ````a```` and ````z````) / ````[0-9]```` means any matching integer between ````0```` and ````9```` (including ````0```` and ````9````) | ````[a-z0-9_\.-]```` an any matching characters between ````a```` and ````z````, ````0```` and ````9````. The remaining characters will be explained in the following sections. 
### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind
Positive Lookahead - Matches a group after the main expression without including it in the result.
Negative Lookahead - Specifies a group that can not match after the main expression (if it matches, the result is discarded).
Positive Lookbehind - Matches a group before the main expression without including it in the result.
Negative Lookbehind - Specifies a group that can not match before the main expression (if it matches, the result is discarded).

## Author

This tutorial was created by Casey Hu and you can find her on <a href="https://github.com/dvtipei">Github</a>