#Strings.js#

###A javascript library for manipulating strings.###

`strings.capitalizeAll(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Capitalizes the first letter of every word in a string.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.capitalizeAll("hello world")` &rarr; "Hello World"

`strings.capitalizeFirst(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Capitalizes the first letter of the first word in a string.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.capitalizeFirst("hello world")` &rarr; "Hello world"

`strings.numberCommas(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Adds commas to a number string for thousands, millions, billions, and so on.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.numberCommas("12345679.312")` &rarr; "12,345,679.312"

`strings.numberLakhs(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Adds commas to a number string for thousands, lakhs, crores, and so on.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.numberLakhs("12345679.312")` &rarr; "1,23,45,679.312"

`strings.numberHundredths(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Rounds a number string, both float and integer, to the nearest hundredth.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.numberHundredths("12345679.312")` &rarr; "12345679.31"

`strings.numberTenths(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Rounds a number string, both float and integer, to the nearest tenth.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.numberTenths("12345679.312")` &rarr; "12345679.3"

`strings.numberPrependZeros(string, number)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Adds zeros before a string so that the string equals a given number of characters. Does nothing to the string if it is already longer than the number of characters.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.numberPrependZeros("1234", 6)` &rarr; "001234"

`strings.reverseLetters(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Reverses the order of the string's letters.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.reverseLetters("hello world")` &rarr; "dlrow olleh"

`strings.reverseWords(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Reverses the order of the string's words.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.reverseWords("hello world")` &rarr; "world hello"

`strings.stripCommas(string)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Remove commas from a string.
<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`strings.stripCommas("123,456,789")` &rarr; "123456789"
