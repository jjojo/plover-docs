## Default Dictionaries

Plover comes supplied with three dictionaries: 

- `main.json`. This contains the default dictionary. It is based on Mirabai Knight's own personal dictionary, which follows a StenEd-style theory. It contains over 140,000 entries and is adequate for anyone learning stenography. Mirabai uses this dictionary professionally for her realtime work.
- `commands.json`. This contains [Plover Control Commands](#plover-control-commands).
- `user.json`. This is available for your personal customizations. `user.json` is a blank dictionary. By default, the `user.json` dictionary is at the bottom of the dictionary list and has the highest priority - it is the first dictionary Plover will use. When you define new strokes, they will get added to this dictionary. This means you can see which strokes you've defined yourself, instead of trying to locate them inside the default dictionaries.

You can add extra dictionaries to Plover, as well. Dictionaries may be located on your system in any directory/folder; they do not have to be in a subdirectory/subfolder of the Plover installation.

> **Note:** We do not recommend you remove the `commands.json` dictionary from the dictionary list. This is because Plover has some concepts that users of other steno software will not be familiar with initially. 

### Dictionary priority

If two dictionaries contain the same steno strokes, Plover will use the one in the dictionary that has the highest priority. The dictionaries in the dictionary list are prioritised from the bottom up. 

By default, the `user.json` dictionary is placed at the bottom of the dictionary list and has the highest priority. If you want new strokes to go to different dictionary (for example, you have your own dictionary already), make sure that dictionary is at the bottom of the list.

> **Note:** With Plover 4.0+, default dictionary priority is now top-down and can be changed.  In the configuration settings, you can select your preferred ordering of dictionary priority to be bottom-up or top-down. 
