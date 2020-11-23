## JSON and RTF/CRE

Plover supports two types of dictionaries:

- **JSON** (the default and recommended format), and 
- **RTF/CRE**. 

RTF/CRE is an import/export format used by proprietary steno software. This means Plover can work with exported dictionaries from Eclipse, ProCAT, Case CATalyst, and other steno software applications.

> **Note:** With Plover 4.0+, there is a plugin `plover-python-dictionary` that allows you to use Python (`.py`) dictionaries. After installing the plugin, you will need to restart Plover before it will let you load Python dictionaries.

### Limitations

There are some limitations with each format:

- RTF dictionaries will cause Plover to take longer to start up and won't have Unicode support. 
- The JSON format that Plover uses is not used or supported by other steno applications. If you want to move or copy your Plover JSON formatted dictionary to another steno software application, you will need to convert it to RTF. 
- The Plover JSON format doesn't have support for stroke metadata. At the moment, Plover doesn't support reading/writing of RTF metadata.
