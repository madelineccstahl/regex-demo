# regex-demo

## Regex Basics by Maddie Stahl

## Summary
Regex filters strings to determine if they fit the criteria of the specified pattern. In this tutorial, the regex used to demonstrate will be that which matches email parameters (= /^[a-zA-Z0-9. _%+-]+@[a-zA-Z0-9. -]+\).

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
Indicated by ( ^ ) and ( $ ), these function as start and end points for a specified string. ^ indicates where to start and $ signifies an end point. These do not indicate matches to any characters and are simply guide points for starts and finishes.

### Quantifiers
Indicated with ( + ), quantifiers set limits for what a string can and can't contain. For example:

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
The + indicates a user must include a character from each sequence within the square brackets at least once. The {2, 6} set a range for the number of times a user can pick from the [a-z.] array.

### OR Operator
Indicated by ( | ). An example would be abc|xyz which is the same as abc or xyz.

### Character Classes
Shortcuts to code sets to be included in the regex. Indicated with ( \ ) followed by a singular charater. Common character classes include:

\b: word boundary. This class is followed by a specified string. Ie, \bmac will indicate macintosh but not insomniac.

\d: digit, same as array [0-9].

\w: ["a-zA-Z0-9_"]: universal regex class, includes most often used characters

### Flags
Allows a user to change the behavior of how Regex searches for a string. There are multiple flags. For JavaScript, the six flags are included below:

i: makes the search case-insensitive

g: search looks for all matches as opposed to the first match only

m: multiline mode (match at the beginning and end of a string or a line)

s: dotall mode, dot ( . ) matches a newline character ( \n )

u: unicode support, corrected processing of surrogate pairs enabled

y: sticky mode, search at an exact position within the text

### Grouping and Capturing
Capturing allows for treating multiple characters as a single unit and is indicated with ( "" ). Grouping refers to storing the captured item within the program's memory so that it can be recalled.

### Bracket Expressions
A bracket expression is indicated with ( `` ). It includes the specific characters that are allowed to match. Ranges of inputs or exact characters are both valid entries, ie. a-z or 0-9.

### Greedy and Lazy Match
Greedy matches ( * ) will return as many matches as possible whereas lazy matches ( ? ) will return as few matches as possible. Each are useful in specific instances depending on whether parameters need to be kept tight or loose. These matches can include partials, strings, single characters and more.

### Boundaries
Boundaries are indicated with ( \b ). They are used to match a word exactly. For instance, cat\b will match with cat, tomcat and bobcat but not catfish, catwalk or catastrophe. The boundary cuts off after cat and requires cat to be included.

### Back-references
Back-references are indicated with ( \1 ). These match a previously created capturing group (of which there can be several, referred to by number, ie \1 or \2 or \3, etc.) with identical text. They can be called again in a new string. An example would look like:

([abc])\3. This will match to the exact same text referenced from the third capturing group.

### Look-ahead and Look-behind
Look-ahead ( ?= ) looks before the indicated text. For instance, the sentence "Oz is a cool dog", a look-ahead ( ?=is a cool dog ) would indicate the word "Oz" since it is before the indicated sentence. This is a positive look-ahead. A positive look-behind would do the opposite and looks like ( ?<= ). A negative look-ahead ( ?! ) will match with anything not directly preceeding the indicated text and the inverse would occur for a negative look-behind. An example of this would be looking through a listing of houses and filtering to exclude ones that are already sold. "House X sold" would be filtered out, leaving you with any houses with a status aside from sold.

### Author
Madeline Stahl is a student at the University of Kansas Full-stack Web Developer Bootcamp program. GitHub: https://github.com/madelineccstahl.
