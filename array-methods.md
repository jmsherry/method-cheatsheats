# Array Methods

## Static Methods (found in the Array constructor)

xxx   `Array.from()` - turns things into an array (e.g. `Array.from(arguments)`)

xxxx  `Array.isArray()` - tests if something is an array

xx    `Array.of()` - A mended version of the Array constructor (ignore) (`Array.of(8)` gives `[8]`; `new Array(8)` gives `[,,,,,,,]`)

## Instance methods (found in each array)

`x`s represent likelyhood of use

xx    `at` - Allows `array.at(-1)` instead of `array[array.length-1]` (* browser support! Polyfill available)

xx    `concat` - Join 2 or more arrays (returns new array)

x     `copyWithin` - Move items around inside the array and returns it

xxxx  `entries` - make an iterator that returns the entries as `[key, value]` (use with `for....of` loops)

xxx   `every` - test if all pass a criterion (return true/false)

xx    `fill` - Fill up part of an array with something

xxxx  `filter` - Find many

xxxx  `find` - Find one (`undefined`, if not found)

xxxx  `findIndex` - Find where one is (`-1` if not found)

x     `flat` - Turn [[1,2], [3,4]] into [1,2,3,4]

x     `flatMap` - Do what `flat` does BUT transform the values like `map` does

xx    `forEach` - iterate (use `for...of` instead because faster, plus `break` and `continue`)

xxx   `includes` - Test if a simple concrete [often primative] value is present (returns true/false)

xx    `indexOf` - Find where simple value is (e.g. `cat` in `['dog', 'cat', 'bird']`)

xxx   `join` - Turn array into string (with separators)

xx    `keys` - make an iterator that returns the keys

x     `lastIndexOf` - Find the last index that a certain item is present (`-1` if not found)

xxx   `map` - create a new array of values by transforming the values in this array

xxxxx `pop` - remove and return the last item

xxxxx `push` - put an item onto the end of the array

xx    `reduce` - reduce all the values in an array down to one (e.g. add them all up)

x     `reduceRight` - Same as reduce but start at the other end

xx    `reverse` - change the order

xxx   `shift` - take something off the front of an array

xxxx  `slice` - copy part of the array

xxx   `some` - test if some items pass a test (returns true/false)

xxx   `sort` - sort things (return `-1`, `0`, `1` to move left, stay, or move right)

xxx   `splice` - delete (and maybe insert) parts of this array (Mutates the actual array)

x     `toLocaleString` - process the things in this array to suit your current location (e.g. currency, time, etc.)

      `toSource` - DON'T USE!!!

x     `toString` - turn into a string (minus the `[]`s)

xx    `unshift` - put something on the front of the array

xx    `values` - make an iterator that returns the values
