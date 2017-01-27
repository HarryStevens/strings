#strings.js#

strings.js is a Javascript library for manipulating strings. Javascript has many [built-in methods for manipulating strings](http://www.w3schools.com/jsref/jsref_obj_string.asp). The functions in this library are meant to supplement those.

To use this library, download `strings.js` or `strings.min.js` from the `src` directory and include it in your HTML file as `<script src="path/to/strings.js"></script>` or `<script src="path/to/strings.min.js"></script>`.

##API Reference##
* [Cases](#cases)
* [Numbers](#numbers)
* [Queries](#queries)
* [Transformations](#transformations)

###<a name="cases" href="#cases">Cases</a>###

Functions for changing the case of words and characters.

<a name="toCamelCase" href="#toCamelCase">#</a> strings.<b>toCamelCase</b>(<i>string</i>)

Transforms a string into camel case.

```js
strings.toCamelCase("Hello world!") // "helloWorld"
```

<a name="toSentenceCase" href="#toSentenceCase">#</a> strings.<b>toSentenceCase</b>(<i>string</i>)

Capitalizes the first letter of the first word in a string.

<a name="toSlugCase" href="#toSlugCase">#</a> strings.<b>toSlugCase</b>(<i>string</i>)

Transforms a string into a slug.

```js
strings.toSlugCase("Hello world!") // "hello-world"
```

<a name="toStartCase" href="#toStartCase">#</a> strings.<b>toStartCase</b>(<i>string</i>)

Capitalizes the first letter of every word in a string.

<a name="toTitleCase" href="#toTitleCase">#</a> strings.<b>toTitleCase</b>(<i>string</i>[, <i>array</i>])

Transforms a string into title case, where the first letter of every word is capitalized except for certain prepositions, articles and conjunctions. Words after a colon will always be capitalized. You can include an optional array to ignore strings of your choice, such as acronyms.

```js
strings.toTitleCase("the quick brown fox jumps over the lazy dog") // "The Quick Brown Fox Jumps over the Lazy Dog"
strings.toTitleCase("james comey to remain on as FBI director", ["FBI"]) // "James Comey to Remain on as FBI Director"
strings.toTitleCase("javascript: a beginner's guide to the language of the web") // Javascript: A Beginner's Guide to the Language of the Web
```

###Numbers###

Functions for manipulating numbers as strings.

<a name="numberCommas" href="#numberCommas">#</a> strings.<b>numberCommas</b>(<i>string</i>)

Adds commas to a number string for thousands, millions, billions, and so on.

<a name="numberDecimals" href="#numberDecimals">#</a> strings.<b>numberDecimals</b>(<i>string</i>, <i>number</i>)

Rounds a number string, both float and integer, to the nearest specified decimal place.

```js
strings.numberDecimals("1", 2) // "1.00"
strings.numberDecimals("1.235", 2) // "1.24"
```

<a name="numberLakhs" href="#numberLakhs">#</a> strings.<b>numberLakhs</b>(<i>string</i>)

Adds commas to a number string for thousands, lakhs, crores, and so on. This is according to the [Indian numbering system](https://en.wikipedia.org/wiki/Indian_numbering_system).

<a name="numberPrependZeros" href="#numberPrependZeros">#</a> strings.<b>numberPrependZeros</b>(<i>string</i>, <i>number</i>)

Adds zeros before a string so that the length of the string equals a given number of characters. Does nothing to the string if it is already longer than the number of characters.
```js
strings.numberPrependZeros("1234", 6) // "001234"
```

###Queries###

Functions for testing strings for certain properties. Will return booleans.

<a name="endsWith" href="#endsWith">#</a> strings.<b>endsWith</b>(<i>string</i>, <i>string</i>[, <i>boolean</i>])

Tests whether a string ends with another string. Defaults to case sensitive, but you can set the third argument to <i>true</i> for case insensitive.

```js
strings.endsWith("Hello world", "LD") // false
strings.endsWith("Hello world", "LD", true) // true
strings.endsWith("Hello world", "LD", false) // false
```

<a name="includes" href="#includes">#</a> strings.<b>includes</b>(<i>string</i>, <i>string</i>[, <i>boolean</i>])

Tests whether a string includes another string. Defaults to case sensitive, but you can set the third argument to <i>true</i> for case insensitive.

```js
strings.includes("Hello world", "WO") // false
strings.includes("Hello world", "WO", true) // true
strings.includes("Hello world", "WO", false) // false
```

<a name="startsWith" href="#startsWith">#</a> strings.<b>startsWith</b>(<i>string</i>, <i>string</i>[, <i>boolean</i>])

Tests whether a string starts with another string. Defaults to case sensitive, but you can set the third argument to <i>true</i> for case insensitive.

```js
strings.startsWith("Hello world", "he") // false
strings.startsWith("Hello world", "he", true) // true
strings.startsWith("Hello world", "he", false) // false
```

###Transformations###

Functions for applying various transformations to strings.

<a name="removeCommas" href="#removeCommas">#</a> strings.<b>removeCommas</b>(<i>string</i>)

Removes commas from a string.

<a name="removeTags" href="#removeTags">#</a> strings.<b>removeTags</b>(<i>string</i>[, <i>array</i>])

Removes HTML tags from a string. You can pass an optional array with the tags you want to keep.

```js
strings.removeTags("<span><i>Hello</i> <b>world</b>!</span>") // Hello world!
strings.removeTags("<span><i>Hello</i> <b>world</b>!</span>", ["i", "span"]) // <span><i>Hello</i> world!</span>
```

<a name="reverseCharacters" href="#reverseCharacters">#</a> strings.<b>reverseCharacters</b>(<i>string</i>)

Reverses the order of a string's characters.

<a name="reverseWords" href="#reverseWords">#</a> strings.<b>reverseWords</b>(<i>string</i>)

Reverses the order of a string's words.

<a name="shuffleCharacters" href="#shuffleCharacters">#</a> strings.<b>shuffleCharacters</b>(<i>string</i>)

Randomly shuffles a string's characters. Uses the [Fischer-Yates shuffle](https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle).

<a name="shuffleCharactersInWords" href="#shuffleCharactersInWords">#</a> strings.<b>shuffleCharactersInWords</b>(<i>string</i>)

Randomly shuffles the characters of each word, but keeps the words in order. Uses the [Fischer-Yates shuffle](https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle).

<a name="shuffleWords" href="#shuffleWords">#</a> strings.<b>shuffleWords</b>(<i>string</i>)

Randomly shuffles a string's words. Uses the [Fischer-Yates shuffle](https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle).
