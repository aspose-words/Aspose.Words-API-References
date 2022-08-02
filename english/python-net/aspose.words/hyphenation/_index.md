---
title: Hyphenation class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides methods for working with hyphenation dictionaries"
type: docs
weight: 480
url: /python-net/aspose.words/hyphenation/
---

## Hyphenation class

Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated.


### Properties

| Name | Description |
| --- | --- |
| [callback](./callback/) | Gets or sets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages. |
| [warning_callback](./warning_callback/) | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |

### Methods

| Name | Description |
| --- | --- |
|[ is_dictionary_registered(language)](./is_dictionary_registered/#str) | Returns False if for the specified language there is no dictionary registered or if registered is Null dictionary, True otherwise. |
|[ register_dictionary(language, stream)](./register_dictionary/#str_bytesio) | Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format. |
|[ register_dictionary(language, file_name)](./register_dictionary/#str_str) | Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format. |
|[ unregister_dictionary(language)](./unregister_dictionary/#str) | Unregisters a hyphenation dictionary for the specified language. |

### See Also

* module [aspose.words](../)

