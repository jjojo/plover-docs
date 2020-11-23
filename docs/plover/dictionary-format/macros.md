
## Macros

Macros can be mapped from a stroke and perform operations on the stroke-level. This means that it can perform actions based on previous strokes, not necessarily on previous words or translations.

### Undo / Delete Last Stroke

- `=undo`

The built-in "undo" macro is assigned to the asterisk key `*`. You can map other strokes to "undo" or "delete last stroke" by creating a stroke where the translation is `=undo`

### Repeat Last Stroke

- `{*+}`

    A stroke mapping to this command will send the last stroke entered. A common stroke to map to repeat-last is the bare number bar; `"#": "{*+}"`; causing `KAT/#/#` to behave like `KAT/KAT/KAT`. 

    Repeat last stroke `{*+}` is very useful for keys that you repeat. For example, when you are moving around text in a document.

**Suggested stroke:** `#`

### Toggle asterisk

- `{*}`

    A stroke mapping to this command will toggle the asterisk key on the last stroke entered. For example, if you had this stroke in your dictionary as Number Bar + Asterisk, `"#*": "{*}"`, when you write `KAT/#*` it will behave as if you wrote `KA*T`. 

    Toggle asterisk `{*}` is useful for when you notice that you should have included an asterisk in your last stroke. For example, you wanted to write the name "Mark" (a person's name), but you wrote "mark" (the noun/verb). At this point, you can use Toggle asterisk `{*}` to correct it. You wouldn't have to erase the word and re-stroke it (this time, with you including the missing the asterisk).

**Suggested stroke:** `#*`

### Retrospectively Add Space

- `{*?}`

    A stroke mapping to this command will add a space between your last stroke and the one before that, splitting apart the two strokes. For example, if your dictionary contained `PER` as "Perfect", `SWAEUGS` as "Situation" and `PER/SWAEUGS` as "Persuasion". If you meant to write "Perfect situation", but saw your output was "Persuasion", you could force these two strokes to be split apart by using the `{*?}` stroke. This means your output would change on the screen from "Persuasion" to "Perfect situation".

**Suggested stroke:** `AFPS` (add space)

### Retrospectively Delete Space

- `{*!}`

    A stroke mapping to this command will delete the space between your last stroke and the one before that. If you wrote "Basket ball" but wanted it to be "Basketball", you could force these strokes together by using the {*!} stroke. Plover will go back and remove the space before your last stroke; As a result, your output would become "Basketball".

**Suggested stroke:** `TK-FPS` (**d**elete space)
