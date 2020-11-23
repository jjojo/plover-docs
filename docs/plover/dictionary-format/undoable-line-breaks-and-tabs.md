
## Undoable Line Breaks and Tabs

When you use [keyboard shortcuts](#keyboard-shortcuts), the asterisk/undo command on Plover will not have any effect. This is a limitation imposed by the fact that most commands will not have a meaningful undo. For example, you wouldn't "undo" a "copy" command. For this reason, `{#return}` and `{#tab}` don't work how many users would expect.

Instead, we must use special characters that can be undone by Plover for new paragraphs and erasable tabs. Specifically: 

- `\n` or `\r` for line breaks. 
- `\t` for tabs. 

For example:

- `{^\n^}{-|}`

    This translation would create a line break without spacing and then capitalize the next word. It can be removed with the asterisk key.

- `{^\t^}`

    This translation presses the tab key without any other spacing. It can be undone with the asterisk key.
