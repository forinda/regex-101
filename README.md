# regex-101
A tech talk intro to Regex
Useful links
- [Regex buddy](https://www.regular-expressions.info/quickstart.html)
```sh
Regular Expression FUll Cheatsheet (For quick look) :)
note: for downloading visit https://buggyprogrammer.com/regular-expression-cheatsheet/
------x-------------------x----------------x------------x----------------x-------------

# -------------- Anchors --------------
^   →  Start of string, or start of line in multiline pattern
\A  →  Start of string
$   →  End of string, or end of line in multi-line pattern
\Z  →  End of string
\b  →  Word boundary
\B  →  Not word boundary
\<  →  Start of word
\>  →  End of word


# ---------- Character Classes --------
\c  →  Control character
\s  →  White space
\S  →  Not white space
\d  →  Digit
\D  →  Not digit
\w  →  Word
\W  →  Not word
\x  →  Hexadecimal digit
\O  →  Octal digit


# --------- Quantifiers -----------------
*     →    0 or more 
{3}   →    Exactly 3
+     →    1 or more 
{3,}  →    3 or more
?     →    0 or 1 
{3,5} →    3, 4 or 5
Add a ? to a quantifier to make it ungreedy.


# ------- Special Characters -------------
\n   →  New line
\r   →  Carriage return
\t   →  Tab
\v   →  Vertical tab
\f   →  Form feed
\xxx →  Octal character xxx
\xhh →  Hex character hh


# --------- Groups and Ranges -------------
.       →  Any character except new line (\n)
(a|b)   →  a or b
(...)   →  Group
(?:...) →  Passive (non-capturing) group
[abc]   →  Range (a or b or c)
[^abc]  →  Not (a or b or c)
[a-q]   →  Lower case letter from a to q
[A-Q]   →  Upper case letter from A to Q
[0-7]   →  Digit from 0 to 7
\x      →  Group/subpattern number "x"
Ranges are inclusive.


# ----------- Assertions ---------------
?=         →  Lookahead assertion
?!         →  Negative lookahead
?<=        →  Lookbehind assertion
?!= or ?<! →  Negative lookbehind
?>         →  Once-only Subexpression
?()        →  Condition [if then]
?()|       →  Condition [if then else]
?#         →  Comment


# ------ Pattern Modifiers --------
g   →  Global match
i*  →  Case-insensitive
m*  →  Multiple lines
s*  →  Treat string as single line
x*  →  Allow comments and whitespace in pattern
e*  →  Evaluate replacement
U*  →  Ungreedy pattern
*   →  PCRE modifier


# ------ String Replacement ------
$n  →  nth non-passive group
$2  →  "xyz" in /^(abc(xyz))$/
$1  →  "xyz" in /^(?:abc)(xyz)$/
$`  →  Before matched string
$'  →  After matched string
$+  →  Last matched string
$&  →  Entire matched string
Some regex implementations use \ instead of $


# ---------- Escape Sequences ------------
\ Escape following character
\Q Begin literal sequence
\E End literal sequence

"Escaping" is a way of treating characters which have a special meaning in regular
expressions literally, rather than as special characters.


# --------- Common Metacharacters ---------
^ 
[
.
$
{
*
(
\
+
)
|
<
>
The escape character is usually \


# ------------ POSIX ----------------
[:upper:]  →  Upper case letters
[:lower:]  →  Lower case letters
[:alpha:]  →  All letters
[:alnum:]  →  Digits and letters
[:digit:]  →  Digits
[:xdigit:] →  Hexadecimal digits
[:punct:]  →  Punctuation
[:blank:]  →  Space and tab
[:space:]  →  Blank characters
[:cntrl:]  →  Control characters
[:graph:]  →  Printed characters
[:print:]  →  Printed characters and spaces
[:word:]   →  Digits, letters and underscore
```

Some awesome more
```js
Let regex;
/* shorthand character classes */
regex = /d/; // matches any digit, short for [0-9]
regex = /D/; // matches non-digits, short for [^0-9]
regex = /S/; // matches non-white space character
regex = /s/; // matches any white space character
regex = /w/; // matches character, short for [a-zA-Z_0-9]
regex = /W/; // matches non-word character [^w]
regex = /b/; // Matches a word boundary where a word character is [a-zA-Z0-9_]
These meta characters boast a pre-defined meaning and make various typical patterns easier to use.
/* matching using quantifiers */
regex= /X./; // matches any character
regex= /X*/; // Matches zero or several repetitions of letter X, is short for {0,}
regex= /X+-/; // matches one or more repetitions of letter X, is short for {1,}
regex= /X?/; // finds no or exactly one letter X, is short for is short for {0,1}.
regex= // d{3}; // matches three digits. {} describes the order of the preceding liberal
regex= // d{1,4} ; // means d must occur at least once and at a maximum of four
A quantifies helps developers to define how often an element occurs.
/* character ranges */
regex = /[a-z]/; // matches all lowercase letters
regex = /[A-Z]/; // matches all uppercase letters
regex = /[e-l]/; // matches lowercase letters e to l (inclusive)
regex = /[F-P]/; // matches all uppercase letters F to P (inclusive)
regex = /[0-9]/; // matches all digits
regex = /[5-9]/; // matches any digit from 5 to 9 (inclusive)
regex = / [a-d1-7]/; // matches a letter between a and d and figures from 1 to 7, but not d1
regex = /[a-zA-Z]/; // matches all lowercase and uppercase letters
regex = /[^a-zA-Z]/; // matches non-letters
/* matching using anchors */
regex = / ^The/; // matches any string that starts with “The”
regex = / end$/; // matches a string that ends with end
regex = / ^The end$/; // exact string match starting with “The” and ending with “End”
/* escape characters */
regex = / a/; // match a bell or alarm
regex = / e/; // matches an escape
regex = / f/; // matches a form feed
regex = / n/; // matches a new line
regex = / Q…E/; // ingnores any special meanings in what is being matched
regex = / r/; // matches a carriage return
regex = / v/; // matches a vertical tab
It is critical to note that escape characters are case sensitive
/* matching using flags */
regex = / i/; // ignores the case in pattern ( upper and lower case allowed)
regex = / m/; // multi-line match
regex = / s/; // match new lines
regex = / x/; // allow spaces and comments
regex = / j/; // duplicate group names allowed
regex = / U/; // ungreedy match
```
