# Learning Regex in Python
Below resources are source/referred/copied from : [link](https://www.python-engineer.com/posts/regular-expressions/)

1. Methods to search for matches
   - match():  looks for pattern at beginning of string
   - search(): returns the first match object
   - finditer() : returns iterator containing all match objects
   - findall() : returns a string list containing matched strings
   - Functions used to modify the match object
     - split() : returns a list where string has been split at each match
     - sub() : replaces one or many matches with a string
2. Methods on a match object
   - group()
   - span()
   - start(), end()
3. Meta characters <br>
All meta characters are: . ^ $ * + ? { } [ ] \ | ( ) 
    - '.' : any character (except newline)
    - '^' : starts with, e.g. "^Hello"
    - '*' : zero or more occurrences e.g. "aix*"
    - '+' : one or more occurrences e.g. "aix+"
    - '{}' : exactly the specified number of occurrences e.g. "al{2}"
    - '[]' : a set of characters e.g. "[a-m]"
    - '\' : signal a special sequence (can also be used to escape special characters e.g. "\d")
    - '()' : capture and group
4. More special sequences <br>
A special sequence is a \ followed by one of the characters in the list below, and has a special meaning:
    - '\d' : matches any decimal digit, equivalent to class [0-9]
    - '\D' : matches any non-digit character, equivalent to [^0-9]
    - '\s' : matches any whitespace character
    - '\S' : matches any non-whitespace character
    - '\w' : matches any alphanumeric character, equivalent to class [a-zA-Z0-9_]
    - '\W' : matches any non-alphanumeric character, equivalent to class [^a-zA-Z0-9_]
    - '\b' : returns a match where specified characters at beginning(or at end) of word, e.g. r"\bain", r"ain\b"
    - '\B' : returns a match where specified characters are present, but not at beginning or end, e.g. r"\Bain", r"ain\B"
    - '\A' : returns a match if specified characters are at beginning of the string, e.g. r"\AThe"
    - '\Z' : returns a match if specified characters are at the end of the string, e.g. r"Spain\Z"
5. Sets <br>
A set is a set of characters inside a pair of square brackets [] with a special meaning. <br> 
Append multiple conditions back-to back, e.g. [aA-Z].
   - A '^' (caret) inside a set negates the expression
   - A '-' (dash) inside a set specifies a range if it's in between, otherwise dash itself
<br>
Examples:
     - [arn] Returns a match where one of the specified characters (a, r, or n) are present
     - [a-n] Returns a match for any lower case character, alphabetically between a and n
     - [^arn] Returns a match for any character EXCEPT a, r, and n
     - [0123] Returns a match where any of the specified digits (0, 1, 2, or 3) are present
     - [0-9] Returns a match for any digit between 0 and 9
     - [0-5][0-9] Returns a match for any two-digit numbers from 00 and 59
     - [a-zA-Z] Returns a match for any character alphabetically between a and z, lower case OR upper case

6. Quantifier
    - '*' : 0 or more
    - '+' : 1 or more
    - '?' : 0 or 1, used when character can be optional
    - '{4}' : exact number
    - '{2,6}' : range numbers (min, max)
7. Conditions
8. Grouping
9. Modification
10. Compilation flags
