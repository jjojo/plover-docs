## Friendly Command Names

In a sufficiently-new Plover version, it's possible to use friendly names for some commands/metas.

For detailed descriptions of the commands, see the other sections.

| Meta | Equivalent |
|------|------------|
| `{^}` | `{:attach}` |
| `{^word}` | `{:attach:^word}` |
| `{word^}` | `{:attach:word^}` |
| `{^word^}` | `{:attach:word}` |
| `{&a}` | `{:glue:a}` |
| `{-\|}` | `{:case:cap_first_word}` |
| `{*-\|}` | `{:retro_case:cap_first_word}` |
| `{~\|word}` | `{:carry_capitalize:word}` |
| `{<}` | `{:case:upper_first_word}` |
| `{*<}` | `{:retro_case:upper_first_word}` |
| `{>}` | `{:case:lower_first_char}` |
| `{*>}` | `{:retro_case:lower_first_char}` |
| `{*($c)}` | `{:retro_currency:$c}` |
| `{#shift(a)}` | `{:key_combo:shift(a)}` |
| `{PLOVER:LOOKUP}` | `{:command:LOOKUP}` |
| `{MODE:CAPS}` | `{:mode:CAPS}` |
| `{.}` | `{:stop:.}` |
| `{,}` | `{:comma:,}` |

Note that currently the `{#a}` form will be interpreted literally in the "Strokes" text box of the Plover "Add Translation" dialog box, however entering a stroke mapped to `{:key_combo:a}` will enter the raw stroke into the text box.
