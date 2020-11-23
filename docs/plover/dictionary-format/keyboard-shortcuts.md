
## Keyboard Shortcuts

Most Plover strokes are just text and formatting operators. Plover handles standard strokes really well. This allows it to handle "undoing" with the asterisk key, as well as automatically handling case and spacing. However, Plover's text and formatting strokes can't send arbitrary key strokes, such as sending keyboard shortcuts.

**Note:** Plover 3.1 introduces new rules for commands that differ slightly from the previous implementation. Before Plover 3.1, commands were used to send symbols because Plover didn't have full Unicode support. *It used to be possible to send "+" by writing `{#plus}`, but the system has been updated.*

- `{#}` is the command operator.

Inside of a command block, you write in what keys you want Plover to simulate. The keys hit in command blocks won't be "undone" when using the asterisk (because you can't backspace a keyboard shortcut). You select the keys by their name. All key names will only refer to the base key. For example, to use letter keys, you just use the corresponding letter (case insensitive) separated by spaces:

- `{#a b c d}` will send "abcd" and will not affect Plover's text formatting or asterisk undo-buffer.

You can also use key names, which is needed when you are accessing a symbol key. For example, on the QWERTY layout there is an equal/plus key in the top right, which you can access by either of its names:

- `{#equal plus}` will send "==". Plover doesn't send modifiers. It just hits the key based on the name. 

If you want to send symbols, though, don't use commands. Commands should be used for keyboard shortcuts only. Instead, use the symbol in your dictionary entry.

### Modifier Names

If you want to use a modifier, use it by name (e.g. `Shift_L`). For convenience, all key names are case insensitive and you can optionally default to the left modifier by dropping the side selector:

| Modifier | Command Key Names (case-insensitive) | 
|----------|----------| 
| Shift | `Shift_L`, `Shift_R`, `shift` | 
| Control |  `Control_L`, `Control_R`, `control` | 
| Alt | `Alt_L`, `Alt_R`, `alt`, `option` | 
| Super | `Super_L`, `Super_R`, `super`, `windows`, `command` | 

For modifiers, use parentheses to delimit where the keys are pressed down.

### Shortcut Key Names

Here are the key names you'll want to use:

| Keys | Command Key Names (case-insensitive) | 
|----------|----------| 
| Letters | `a`, `b`, …, `z` |
| Accented Letters (international layouts) | `udiaeresis`, `eacute`, etc.  |
| Numbers | `0`, `1`, …, `9` | 
| Control Keys |  `Escape`, `Tab`, `Caps_Lock`, `space`, `BackSpace`, `Delete`, `Return`, etc. | 
| F-Keys | `F1`, `F2`, …, `F12` | 
| Common Named Keys | `asciitilde` (~), `asciicircum` (^), `equal`, `minus`, `slash`, `backslash`, `comma`, `colon`, etc. |
| Media Keys | **Common**: `AudioRaiseVolume`, `AudioLowerVolume`, `AudioMute`, `AudioNext`, `AudioPrev`, `AudioStop`, `AudioPlay`, `AudioPause`, `Eject`, **Mac**: `MonBrightnessUp`, `MonBrightnessDown`, `KbdBrightnessUp`, `KbdBrightnessDown`, **Windows**: `Back`, `Forward`, `Refresh`. Note: Linux supports supports any XF86 keyname. |

Consult the code for the [full list of supported keyboard shortcut keys](https://github.com/openstenoproject/plover/blob/master/plover/key_combo.py#L21). 

Note that a particular key name will send an unmodified key. For example, for many typical keyboard layouts <code>{#braceleft}</code> will cause <code>[</code> to be outputted while <code>{#shift(braceleft)}</code> will cause <code>{</code> to be outputted.

Most symbols (e.g. `+, =, ~, r`) can just be included directly in the definition. But some symbols are part of the dictionary syntax and so need to be escaped: 

| Symbol | Escaped Form | 
|----------|----------| 
| `"` | `\"`   |
| `\` | `\\`   |
| `{` | `\\{`  |
| `}` | `\\}`  |

### Example Shortcuts

Here are some shortcuts. They are in JSON format:

- `"STPH-G": "{#right}"` — right arrow on the keyboard, for moving the cursor to the right once
- `"SKWR-G": "{#shift(right)}"` — shift and right arrow on the keyboard, for selecting one character
- `"SKWR-BG": "{#control(shift(right))}"` — shift, control, and right arrow on the keyboard, for selecting one word to the right on Windows/Linux
- `"SKWR-BG": "{#option(shift(right))}"` — option (alt), control, and right arrow on the keyboard, for selecting one word to the right on Mac

These next strokes are not particularly useful, but they show you what you can do with the command syntax:

- `"TKAO*UP": "{#control(c v v v)}"` — copy, then paste 3 times
- `"SKPH-Z": "{#control(z shift(z))"` — program-dependent, but possibly "undo/redo". Notice how the first z has only the control operator, and the second has both the control and the shift operator.

Commands are case insensitive - adding capitals will not affect the output. `{#control(z shift(z))` is the same as `"{#CONTROL_L(Z SHIFT(Z))}"`

### "Do Nothing" Translation

You can use the keyboard shortcut syntax (`{#}`) if you want a stroke that effectively does nothing. For example: a null or canceled stroke, which doesn't affect formatting, doesn't output anything, and cannot be "undone" with the asterisk key. A stroke mapped to `{#}` will effectively do nothing but show up in your logs.

- `{#}` an effective "null" stroke.

See also: [Canceling Formatting of Next Word](#canceling-formatting-of-next-word)
