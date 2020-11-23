## Text Formatting

### Prefixes, Infixes, and Suffixes

Strokes can be attached at the beginning and/or end using the "attach" operator. You can also use some of the built-in orthographic rules that Plover uses for creating intelligent strokes.

- `{^}` is the attach operator.
- `{^ish}` is an orthographic-aware suffix that will add "ish" to the end of the previous word. E.g. `RED/EURB` will output `reddish`. Note: addition of a second "d" caused by Plover's understanding of English orthography.
- `{^}ish` is a suffix with the text outside the operator—this means that the text will simply be attached without grammar rules. Using this stroke in the previous example would give instead `redish`.
- `{^-to-^}` is an infix, e.g. `day-to-day`.
- `{in^}` is a prefix, e.g. `influx`.
- Most custom punctuation entries will take advantage of the attach operator, e.g. `{^—^}` for an emdash.

### Glue Operator (Numbers, Fingerspelling)

Glue is sort of like the [attach operator](#prefixes-infixes-suffixes) above, except that "glued" strokes only attach to neighboring "glue" strokes.

Translations containing *only* digits are glued, allowing you to output multiple number strokes to make a large number.

- `{&}` is the glue operator.
- `{&a}`, `{&b}`, `{&c}`, etc. are how the fingerspelling alphabet is made.
- `{&th}` is a multiletter glue stroke, which can be useful (`TH*` in the default dictionary)

Because glued translations only glue to other glued translations, they won't attach to regular words. This gives us some power because you can write:

`THR/-R/#H/#A/KATS` to get "there are 45 cats" and only `#H` (4) and `#A` (5) are "glued" to each other.

### Capitalizing

Capitalizing a word means turning the first letter into a capital, e.g. proper nouns and in titles. Usually your dictionary has capitals pre-defined, but there are times when you need to capitalize a word on the go.

#### Capitalize Next Word

- `{-|}`

The next word will have a capitalized first letter. In the default dictionary, we have `"KPA": "{-|}"`, which will capitalize the next word; and `"KPA*": "{^}{-|}"` which omits a space and capitalizes the next word. That last stroke would let you writeLikeThis. This formatting style is called "camel case', which some programmers use in their work. 

Capitalize next word can also be used in name titles, like `Ms. {-|}`.

**Default strokes:**

- `KPA`: `{-|}` (think "cap")
- `KPA*`: `{^}{-|}` (also suppresses space)

#### Capitalize Last Word

- `{*-|}`

The last stroke word will have a capitalized first letter. This is useful in case you realize that a word should be capitalized after you've written it. It can also be used in a stroke, like in `{*-|}{^ville}`. This would capitalize the last word and attach to it. This would be useful for town names on the fly, such as `Catville`.

**Suggested stroke:** `KA*PD`

### Carrying Capitalization

- `{~|text}` or `{^~|text^}` where the attach operator is optional and the text can be changed.

In English, we have punctuation that doesn't get capitalized, but instead the next letter gets the capitalization. For example, if you end a sentence in quotes, the next sentence still starts with a capital letter! `"You can't eat that!" The baby ate on.` 

In order to support this, there is a special pre/in/suffix syntax that will "pass on" or "carry" the capitalized state. You might find this useful with quotes, parentheses, and words like `'til` or `'cause`. 

The default dictionary for Plover should use these operators where appropriate.

```json
{
  "KW-GS": "{~|\"^}",
  "KR-GS": "{^~|\"}",
  "KA*US": "{~|'^}cause",
  "PREPB": "{~|(^}",
  "PR*EPB": "{^~|)}"
}
```

 For a newline, the syntax would be `{^~|\n^}`.

### Uppercasing (CAPS)

See [Output Modes](#output-modes) for CAPS mode, which acts like CAPS lock on a regular keyboard. Alternatively, you can use a [Keyboard Shortcut](#keyboard-shortcuts) set to `{#Caps_Lock}` to activate the system CAPS lock like you can on your keyboard.

**Suggested stroke:** `"KA*PS": "{MODE:CAPS}"`

#### Uppercase Next Word

- `{<}`

Output next stroke in capital letters, e.g. `{<}cat` → `CAT`

**Suggested stroke:** `KPA*L` (cap all)

#### Uppercase Last Word

- `{*<}`

Rewrite last word in capital letters, e.g. `cat{*<}` → `CAT`

**Suggested stroke:** `*UPD`

### Lowercasing

#### Lowercase Next Word

- `{>}`

Forces the next letter to be lowercase, e.g. `{>}Plover` → `plover`

**Suggested stroke:** `HRO*ER` (lower)

#### Lowercase Last Word

- `{*>}`

Rewrite the last word to start with a lowercase letter, e.g. `Plover{*>}` → `plover`

**Suggested stroke:** `HRO*ERD` (lowered)

### Canceling Formatting of Next Word

In order to cancel formatting of the next word, use the empty meta tag as your definition:

- `{}`

Using `{}` in front of a arrow key commands, as in `{}{#Left}`, is useful if the arrow key commands are used to move cursor to edit text. Canceling formatting actions for cursor movement prevents Plover from, for instance, capitalizing words in middle of a sentence if cursor is moved back when the last stroke, such as `{.}`, includes action to capitalize next word.

See also the ["do nothing" translation](#do-nothing-translation)

### Format Currency

There is a built-in meta in Plover that allows you to format the last-written number as currency. The format is `{*($c)}` where `$` is any currency symbol you'd like, and `c` is the amount, formatted in standard currency format, with either no decimals or two. Commas are added every 3 numbers before the decimal automatically.

- `{*($c)}`: Standard English dollars
  + `23{*($c)}` → $23
  + `2000.5{*($c)}` → $2,000.50
- `{*($c CAD)}`: You can include other text, e.g. when specifying a currency's country
  - `100{*($c CAD)}` → $100 CAD
- `{*(c円)}`: The symbol can be placed on either side of the number, which often happens in languages other than English and in certain regions.
  - `2345{*(c円)}`: 2,345円

Here are some other currency symbols, in case you need to copy-paste them into your entries: £, ¥, €, $, ₩, ¢
