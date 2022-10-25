# Regular Expression Tutorial



## Summary

Regular expressions are effect tools used to extract information from text by searching for matches of a specific search pattern. Regular expressions or regex for short, range from validation to parsing/replacing strings,passing through translating data to other formats and web scraping. In this tutorial I will explain further how effective a tool regex can be within most programming languages. 

## Table of Contents

- [Regular Expression Tutorial](#regular-expression-tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components
Regular expressions are made up of several components. This regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ includes the following:

Anchors ^ $
Captures and Groups ([a-z0-9_\.-]+)
Quantifiers + {}
Bracket Expressions [ ]
Character Classes [a-z\d] etc

### Anchors
Anchors belong to the family of regex tokens that don't match any characters, but that assert something about the string or the matching process. Anchors assert that the engine's current position in the string matches a well-determined location: for instance, the beginning of the string, or the end of a line.

Anchor marks signify the beginning and end of a string, line or word. 

/^[information]$/

The ^ sign is the beginning. 
The $ sign is the end. 


### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. The following table lists examples of quantifiers

Greedy quantifier	Lazy quantifier	  Description
*	                 *?	              Matches zero or more times.
+	                 +?	              Matches one or more times.
?	                 ??	              Matches zero or one time.
{ n }	             { n }?	          Matches exactly n times.
{ n ,}	             { n ,}?	      Matches at least n times.
{ n , m }	         { n , m }?	      Matches from n to m times.

The quantities n and m are integer constants. Ordinarily, quantifiers are greedy. They cause the regular expression engine to match as many occurrences of particular patterns as possible. Appending the ? character to a quantifier makes it lazy. It causes the regular expression engine to match as few occurrences as possible. 


### Grouping Constructs

A regular expression grouping construct is similar to what a parenthetical statement is to math operations. Group constructs bind expressions together to evaluate specific information in a specific order. Parentheses ( ) signify a capture group. This is a sequence of character classes, brackets, quantifiers, and other elements for the regex to match, just within that group.



### Bracket Expressions

The bracket [ ] grouping construct groups evaluation criteria together for evaluation. The regular expression will consider all data in the group [ ] for matching to remain True.

Some examples of grouping constructs are listed below: 

[a-z] or [A-Z]: This indicates a character range from one character to another character. This will return True if any of the characters in the string contain the characters within the range. This will return False if all of the characters are out of the range of characters provided.

[0-9]: This indicates a number range from one number to another number. This will return True if any of the numbers in the string contain the numbers in the range. This will return False if all of the numbers are out of the range of numbers provided.

[abcd1234]: This indicates specific characters abcd123 that are to be matched in a string. This will return True if any of the abcd1234 characters in the string contain the characters specified in the regular expression group. This will return False if the complete string doesn't contain the abcd1234 characters provided in the regular expression group.

### Character Classes

Character classes distinguish kinds of characters such as, for example, distinguishing between letters and digits.

This regex has three groups:
([a-z0-9_\.-]+)
([\da-z\.-]+)
([a-z\.]{2,6})
Capturing groups are used to extract the string of the regex within the parentheses. This includes the character sets within the square brackets and the quantifiers such + outside of the square brackets.

### The OR Operator

Logical “or” is achievable by combining results of multiple regular expressions using the native “or” logical feature of your programming language of choice. This can sometimes be simpler and easier for others to maintain in the future, with only minimal performance impacts over moderate data-sets. The "or" symbol in JavaScript is | 

### Flags

A flag is an optional parameter to a regex that modifies its behavior of searching.
A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character.

In JavaScript regex, we have a total of 6 flags, each serving a different purpose.
Flag	Name	                   Modification
i	 Ignore Casing	      Makes the expression search case-insensitively.
g	    Global	          Makes the expression search for all occurrences.
s	    Dot All	          Makes the wild character . match newlines as well.
m	    Multiline	      Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
y	    Sticky	          Makes the expression start its searching from the index indicated in its lastIndex property.
u	    Unicode	          Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.


### Character Escapes

The backslash in a regular expression precedes a literal character. You also escape certain letters that represent common character classes, such as \w for a word character or \s for a space. The following example matches word characters (alphanumeric and underscores) and spaces.

## Author

The Author is John Bynum. An up and coming web developer currently enrolled in Rutger's Bootcamp 2022. Link to my github is github.com/iexclusive21
