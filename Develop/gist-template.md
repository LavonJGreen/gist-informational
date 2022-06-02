# URL Matching a Regex Tutorial

A regex pattern matches a target string. The pattern is composed of a sequence of atoms. An atom is a single point within the regex pattern which it tries to match to the target string. The simplest atom is a literal, but grouping parts of the pattern to match an atom will require using ( ) as metacharacters.

## Summary

## Example:

# Regex Informational: URL matching.
A regex pattern matches a target string. The pattern is composed of a sequence of atoms. An atom is a single point within the regex pattern which it tries to match to the target string. The simplest atom is a literal, but grouping parts of the pattern to match an atom will require using ( ) as metacharacters.

## Example:

```regexp
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ 
```
## Summary:
A Regex "regular expression" is a series of special characters that can check a string for matches that meet specific criteria. This informational will explore a little more into what those special characters are, and how we can easily read them.

## Example:

```regexp
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ 
```

## Regex Character Identification:

-`/` Initiates regex

-`^` This is known as the beginning anchor .

-`(` Used to create a capture group.

-`https` This indicates a sub-expression string that should be matched.

- `?` This is a Greedy quantifier 

- `\/\/` This is an escaped character 

- `)` This Ends the capture grouped.

- `(` Begins captured group.

- `[` Begins bracket list.

- `/d` Is a metacharacter indicating any one digit character (0-9)

- `a-z` Indicates lower case letters between a-z.

- `\.` Escape sequence denoting the character `.`

- `-` Indicates `-` character

- `]` Ends bracket list.

- `+`  characters may occur one or more times.

- `)` Ends captured group.

- `\.` Escape sequence denoting the character `.`

- `(` Begins captured group.

- `[` Begins bracket list.

- `a-z.` Indicates lower case letters between a-z.

- `]` Ends bracket list.

`{2,6}` Occurence may occur from 2 to 6 times.

- `)` Ends captured group.

- `(` Begins captured group.

- `[` Begins bracket list.

- `/` Escapes regex to match the character `/`

- `\w` Is a character class indicating any dingle Word Characters. Those are any characters including a-z, A-Z, 0-9, and _.

- `.` Escape sequence denoting the character `.`

- `-` Indicates `-` character

- `]` Ends bracket list.

- `*` Greedy quantifier denoting that the previous bracket list characters may occur zero or more times

- `)` Ends captured group.

- `*` Greedy quantifier indicating that the entire previous captured group may occur zero or more times.

- `/` Escapes regex to denote a regular `/` character

- `?` Greedy quantifier indicating previous `/` character may have 0 or 1 occurrences.

- `$` Position acnhoring that ends the string.

- `/` Ends Regex.

## Table of Contents:

- [Anchors](#Anchors)
- [Quantifiers](#Quantifiers)
- [Character Classes](#Character-Classes)
- [Grouping and Capturing](#Grouping-and-Capturing)
- [Bracket Expressions](#Bracket-Expressions)
- [Greedy and Lazy Match](#Greedy-and-Lazy-Match)

## Regex Components

### Anchors
Anchors are regex tokens that don't match any characters but that say or assert something about the string or the matching process. Anchors inform us that the engine's current position in the string matches a determined location: for example, the beginning of the string/line, or the end of a string/line.

 ^ --- A string will begin with the characters that follow the ^.
    $ --- A string will end with the characters that precede the $.
    \A --- A match must occur at the start of a string.
    \Z --- A match must occur at the end of a string or before a new line \n.
    \z --- A match must occur at the end of a string.
    \G --- A match must occur at the point where a previous match ended.
    \b --- A match must match positions between a alphanumeric or "word" character and a non-alphanumeric character.
    \B --- A match must NOT match positions between a alphanumeric or "word" character and a non-alphanumeric character.
    
### Quantifier
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

 * --- Matches a pattern 0 or more time.
 + --- Matches a pattern 1 or more times.
 ? --- Matches a pattern 0 or 1 time only.
 { n } --- Matches a pattern exactly n times
 { n, } --- Matches a pattern at least n times
 { n, x } --- Matches a pattern at least n times, but no more than x times.
    
### Charcter Class
In the context of regular expressions, a character class is a set of characters enclosed within square brackets. It specifies the characters that will successfully match a single character from a given input string.

 [characters] --- Matches any single character in the character group.
 [^characters] --- Matches exclude any single character in the character group.
 . --- Matches any character (except a newline character \n).
 \d --- Matches any arabic numeral (0-9).
 \w --- Matches any basic Latin alphanumeric including _.
 \s matches a single whitespace “ “, including tabs and line breaks.
 
 ### Grouping and Capturing
 Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses. For example, the regular expression (dog) creates a single group containing the letters "d" "o" and "g" .
  
  ( sub ) --- captures match and assigns a number.
  (?< name > sub ) or (?' name ' sub) --- captures match and assigns a named group.
  (?: sub ) --- defines a non-capturing group.
  
  ### Bracket Expressions
  A bracket expression (an expression enclosed in square brackets, "[]" ) is an RE that shall match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression.
  
  ### Greedy and Lazy Match
  
  A greedy match means that the regex engine (the one which tries to find your pattern in the string) matches as many characters as possible. For example, the regex 'a+' will match as many 'a' s as possible in your string 'aaaa' .
  
  The lazy mode of quantifiers is an opposite to the greedy mode. It means: “repeat minimal number of times”. We can enable it by putting a question mark '?' after the quantifier, so that it becomes *? or +? or even ?? for '?'
  
  ## Author 
  
  This informational was Written by Lavon Green, a Front End developer, behavioral counselor who was born and raised on the Island of Jamaica and moved to Brookly, NY at the age of 9.
  His git hub is linked here https://github.com/LavonJGreen
  