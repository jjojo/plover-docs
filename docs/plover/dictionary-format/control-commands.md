## Control Commands

You can control some aspects of Plover with [strokes](#strokes-and-dictionaries). Plover's default dictionary (`commands.json`) contains these commands:

| Command name | Command | Default Stroke | Description |
|----------|----------| ----------| ----------| 
| Add Translation | `{PLOVER:ADD_TRANSLATION}` | `TKUPT` (think DUPT for "Dictionary UPdaTe") | Opens a translation window where you can enter a stroke and translation text to create a new dictionary entry. |
| Disable Output | `{PLOVER:SUSPEND}` | `PHRO*F` (think PLOF for "PLover OFf") | Stop translating steno. With a keyboard machine, you will be able to type normally again. |
| Enable Output | `{PLOVER:RESUME}` | `PHROPB` (think PLON for "PLover ON") | Re-enable Plover's output. You can write this stroke to switch back from your keyboard into steno mode. |
| Toggle Output | `{PLOVER:TOGGLE}` | `PHROLG` (think PLOLG, for PLOver toGGLe) | Toggle between output being enabled and disabled. |


| Command name| Command | _Suggested_ Stroke | Description |
|----------|----------| ----------| ----------| 
| Look Up Stroke | `{PLOVER:LOOKUP}` | `PHR*UP` | Open a search dialog that you write a translation into to get a list of entries in your dictionaries. |
| Configure | `{PLOVER:CONFIGURE}` | `PHROFG` (think PLOFG, for PLOver conFiG) | Open and focus the Plover configuration window. |
| Focus | `{PLOVER:FOCUS}` | `PHROFBGS` (think PLOFKS, for PLOver focus) | Open and focus the main Plover window. |
| Quit | `{PLOVER:QUIT}` | `PHROBGT` (think PLOKT, for PLOver **qu**i**t**) | Quit Plover entirely. |
