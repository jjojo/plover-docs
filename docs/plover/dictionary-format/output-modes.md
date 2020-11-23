

## Output Modes

- `{MODE:}` is the mode operator

Plover supports special character casing, such as CAPS LOCK and Title Case. It also supports replacing its implicit space with other characters. This is useful for when you want to write_in_snake_case.

**Output modes** are activated with a special syntax in your dictionary. They can be a stroke or just part of a stroke. They can then be turned off with a special reset command. 

An example flow for CAPS LOCK might be:

1. Turn on CAPS LOCK.
1. Write in capital letters.
1. Turn off CAPS LOCK.

However, there's nothing stopping you from building in output modes into your strokes. For example, you might want your new paragraph stroke to reset the case mode, no matter what.

### Reset Command

You can reset the output mode to its default with `{MODE:RESET}`. 

> **Important**: We recommended you have a reset output mode command, so that you can always reset Plover's output mode. This is in case you change it by accident. 

- `{MODE:RESET}`: Reset the case and space character. We recommended this for getting out of any custom output mode.
    For example: `"R-R": "{^~|\n^}{MODE:RESET}"` and `"TPEFBG": "{#escape}{MODE:RESET}"`
- `{MODE:RESET_CASE}`: Exit caps, lower, or title case.
- `{MODE:RESET_SPACE}`: Use spaces as normal.

### Modes

There are some built-in modes you can use:

| Dictionary Syntax | Sample Output | 
|-----------|---------|
| `{MODE:CAPS}` | THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG. |
| `{MODE:TITLE}` | The Quick Brown Fox Jumps Over The Lazy Dog. | 
| `{MODE:LOWER}` | the quick brown fox jumps over the lazy dog. |
| `{MODE:CAMEL}` | theQuickBrownFoxJumpsOverTheLazyDog. |
| `{MODE:SNAKE}` | The_quick_brown_fox_jumps_over_the_lazy_dog. |

### Custom Modes

You can define your own custom modes with the `SET_SPACE:` operator. This allows you to replace the space that Plover outputs with anything. Plover's snake-mode is the same as `SET_SPACE:_`. 

Here are some other examples:

| Dictionary Syntax | Sample Output | 
|---------|-----------|
| `{MODE:SET_SPACE:}` | Thequickbrownfoxjumpsoverthelazydog. |
| `{MODE:SET_SPACE:-}` | The-quick-brown-fox-jumps-over-the-lazy-dog. | 
| `{MODE:SET_SPACE:😁}` | The😁quick😁brown😁fox😁jumps😁over😁the😁lazy😁dog. | 

### Summary of suggested commands you can cut and paste into your dictionary

Here is a summary of the suggested commands you can cut and paste into your personal dictionary:

```json
{
"PHR*UP":"{PLOVER:LOOKUP}",
"PHROFG":"{PLOVER:CONFIGURE}",
"PHROFBGS":"{PLOVER:FOCUS}",
"PHROBGT":"{PLOVER:QUIT}",
"KA*PD":"{*-|}",
"KA*PS":"{MODE:CAPS}",
"KPA*L":"{<}",
"*UPD":"{*<}",
"HRO*ER":"{>}",
"HRO*ERD":"{*>}",
"#":"{*+}",
"#*":"{*}",
"AFPS":"{*?}",
"TK-FPS":"{*!}"
}
```
> **Note:** The final entry must not have a trailing comma.
