# String Methods

## Pre-Notes

1. A `searchTerm` is something like 'cat'
2. A Regular Expression is a string that describes a pattern
3. In general searches will find the first match and stop
4. By making a search 'global' (with a regular expression) you can find all the matches
5. Browsers represent letters with numbers (aka. Unicode). They can encode those numbers in different formats: raw unicode; UTF-8 (8-bits), UTF-16 (16 bits, hence can hold more letters, especially international characters), etc.
6. locale - e.g. the accented version of a word vs non-accented (`'réservé'` vs `'RESERVE'`)
7. ** REMEMBER ** - Strings are primitives and therefore immutable. Methods will return a new string, rather than changing the existing one!

## Static Methods

String.raw() - gets a raw string from template strings (ignore)

String.fromCharCode() - UTF-16 code units (ignore)

String.fromCodePoint() - creates a string from 'code points' (ignore)

## Instance Methods

xx    `at` - Allows `array.at(-1)` instead of `array[array.length-1]` (* browser support! Polyfill available)

x     `charAt` - Finds that character at a certain point (use square brackets `str[2]`)

x     `charCodeAt` - Finds the character code (UTF-16) at that point

x    ` codePointAt` - Finds the codepoint at that point (general unicode)

x     `concat` - Join strings

xx    `endsWith` - check end of string for `<some string>` (end is adjustable)

xxx   `includes` - checks entire string for `<some string>` (search start point is adjustable) returns boolean

xx    `indexOf` - Finds the first position of `<some string>`

x     `lastIndexOf` - Finds the last position of `<some string>`

x     `localeCompare` - comparing 2 strings of different locales (when they have non-standard letters, like ë)

xxx   `match` - like includes but uses Regular Expressions

x     `matchAll` - like match, but returns an iterator (generator fn that can be used later)

x     `normalize` - turns unicode codepoints into normal string

xx    `padEnd` - add some characters at the end to make it a certain length

xx    `padStart` - same as padEnd, but at the start

xx    `repeat` - create a string that repeats another `n` times

xxx   `replace` - replaces string/regex with another value (often `''` to remove things) - **IF PATTERN IS STRING only the first instance is replaced**

x     `replaceAll` - like replace but global

xxx   `search` - Search a string with a regular expression

xxxx  `slice` - copy parts of a string

xxxx  `split` - turn a string into an array (splitting it on a searchTerm)

xx    `startsWith` - check start of string for `<some string>`(start is adjustable)

`substring` - **use slice**
`substr` - legacy! **use slice**

x     `toLocaleLowerCase` - transforms to regional lowercase

x     `toLocaleUpperCase` - transforms to regional uppercase

xxxx  `toLowerCase` - transforms to lowercase

`toString` - Aliases to valueOf() for strings

xxxx  `toUpperCase` - transforms to uppercase

xxx   `trim` - removes whitespace from both ends

x     `trimEnd/trimRight` - removes whitespace from end

x     `trimStart()/trimLeft` - removes whitespace from start

`valueOf` - converts Constructed string objects e.g. `String(2)` to basic strings `'2'`. ** Usually called internally, not in code!! **

      `String.prototype[@@iterator]()` - for interal use (gets the generator fn to iterate over the string with. Used by `for...of`, etc.)
