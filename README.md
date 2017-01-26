#strings.js#

strings.js is a Javascript library for manipulating strings. Javascript has many [built-in methods for manipulating strings](http://www.w3schools.com/jsref/jsref_obj_string.asp). The functions in this library are meant to supplement those.

Each function can be used in two ways. First, a function can be used in the `strings` namespace (e.g. `strings.method("Hello world!")`); second, it can be used as a modification to the native Javascript `String` object, which allows for applying multiple functions to a single string (e.g. `"12345.15".numberDecimals(1).numberCommas()` &rarr; 12,345.2).

##Functions##

<a name="numberCommas" href="#numberCommas">#</a> strings.<b>numberCommas</b>(<i>string</i>)

Adds commas to a number string for thousands, millions, billions, and so on.

```js
strings.numberCommas("12345679.312"); // "12,345,679.312"
```

<a name="numberDecimals" href="#numberDecimals">#</a> strings.<b>numberDecimals</b>(<i>string</i>, <i>number</i>)

Rounds a number string, both float and integer, to the nearest specified decimal place.

```js
strings.numberDecimals("12345679.312", 4); // "12345679.3120"
```

<a name="numberLakhs" href="#numberLakhs">#</a> strings.<b>numberLakhs</b>(<i>string</i>)

Adds commas to a number string for thousands, lakhs, crores, and so on.

```js
strings.numberLakhs("12345679.312"); // "1,23,45,679.312"
```

<a name="numberPrependZeros" href="#numberPrependZeros">#</a>strings.<b>numberPrependZeros</b>(<i>string</i>, <i>number</i>)

Adds zeros before a string so that the length of the string equals a given number of characters. Does nothing to the string if it is already longer than the number of characters.

```js
strings.numberPrependZeros("1234", 6) // "001234"
```

<a name="removeCommas" href="#removeCommas">#</a> strings.<b>removeCommas</b>(<i>string</i>)

Remove commas from a string.

```js
strings.removeCommas("123,456,789") // "123456789"
```

<a name="reverseCharacters" href="#reverseCharacters">#</a> strings.<b>reverseCharacters</b>(<i>string</i>)

Reverses the order of the string's characters.

```js
strings.reverseCharacters("hello world") // "dlrow olleh"
```

<a name="reverseWords" href="#reverseWords">#</a> strings.<b>reverseWords</b>(<i>string</i>)

Reverses the order of the string's words.

```js
strings.reverseWords("hello world") // "world hello"
```

<a name="shuffleCharacters" href="#shuffleCharacters">#</a>`strings.shuffleCharacters(string)` OR `string.shuffleCharacters()`

Randomly shuffles a string's characters. Uses the [Fischer-Yates shuffle](https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle).

```js
strings.shuffleCharacters("hello world") // "r holledowl"
```

<a name="shuffleWords" href="#shuffleWords">#</a> strings.<b>shuffleWords</b>(<i>string</i>)

Randomly shuffles a string's words. Uses the [Fischer-Yates shuffle](https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle).

```js
strings.shuffleWords("The quick brown fox jumps over the lazy dog.") // "brown lazy the The fox dog. quick over jumps"
```

<a name="toCamelCase" href="#toCamelCase">#</a> strings.<b>toCamelCase</b>(<i>string</i>)

Transforms a string into camel case.

```js
strings.toCamelCase("Hello world!") // "helloWorld"
```

<a name="toSentenceCase" href="#toSentenceCase">#</a> strings.<b>toSentenceCase</b>(<i>string</i>)

Capitalizes the first letter of the first word in a string.

```js
strings.toSentenceCase("hello world") // "Hello world"
```

<a name="toSlugCase" href="#toSlugCase">#</a> strings.<b>toSlugCase</b>(<i>string</i>)

Transforms a string into a slug.

```js
strings.toSlugCase("Hello world!") // "hello-world"
```

<a name="toStartCase" href="#toStartCase">#</a> strings.<b>toStartCase</b>(<i>string</i>)

Capitalizes the first letter of every word in a string.

```js
strings.toStartCase("hello world") // "Hello World"
```

<a name="toTitleCase" href="#toTitleCase">#</a> strings.<b>toTitleCase</b>(<i>string</i>[, <i>array</i>])

Transforms a string into title case, where the first letter of every word is capitalized except for certain prepositions, articles and conjunctions. You can include an optional array to ignore strings of your choice, such as acronyms.

```js
strings.toTitleCase("james comey to remain on as FBI director", ["FBI"]) // "James Comey to Remain on as FBI Director"
```
