---
title: Hyphenation class
linktitle: Hyphenation class
articleTitle: Hyphenation class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Hyphenation class. Provides methods for working with hyphenation dictionaries"
type: docs
weight: 530
url: /nodejs-net/aspose.words/hyphenation/
---

## Hyphenation class

Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated.
To learn more, visit the [Working with Hyphenation](https://docs.aspose.com/words/nodejs-net/working-with-hyphenation/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [callback](./callback/) | Gets or sets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages. |
| [warningCallback](./warningCallback/) | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |

### Methods

| Name | Description |
| --- | --- |
|[ isDictionaryRegistered(language)](./isDictionaryRegistered/#string) | Returns ``false`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``true`` otherwise. |
|[ registerDictionary(language, stream)](./registerDictionary/#string_buffer) | Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format. |
|[ registerDictionary(language, fileName)](./registerDictionary/#string_string) | Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format. |
|[ unregisterDictionary(language)](./unregisterDictionary/#string) | Unregisters a hyphenation dictionary for the specified language. |

### See Also

* module [Aspose.Words](../)

