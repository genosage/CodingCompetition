Many people occasionally mis-time holding the shift key while typing, thus causing the capitalization at the beginning of their sentences to be incorrect. Thankfully, Microsoft Word engineers created a feature many years ago to automatically fix this for users. To pay homage to this feature, which is now often taken for granted, this problem focuses on a simple version of the feature: where the only time a capital should be used is at the beginning of a sentence (we'll ignore things like proper nouns and abbreviations).

#### Input definition

The input will be a series of lines, each of which contains one or more sentences. The beginning of a sentence is the first letter of the line or the first letter following a previous sentence. The end of a sentence is marked by a period, question mark, or exclamation point. The input will be terminated with an empty line.

#### Output definition

The same format as the input, only the first letter of each sentence must be capitalized and no other letters may be capitalized.

#### Example input

```
This is a well-capitalized sentence. this is not. Neither is a terribly Interesting sentence.
this is a second line. Why are these sample sentences so blah?
```
#### Example output

```
This is a well-capitalized sentence. This is not. Neither is a terribly interesting sentence.
This is a second line. Why are these sample sentences so blah?
```