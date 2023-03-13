﻿---
title: TxtListIndentation class
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies how list levels are indented when document is exporting to [SaveFormat.TEXT](../../aspose.words/saveformat/#TEXT) format"
type: docs
weight: 800
url: /python-net/aspose.words.saving/txtlistindentation/
---

## TxtListIndentation class

Specifies how list levels are indented when document is exporting to [SaveFormat.TEXT](../../aspose.words/saveformat/#TEXT) format.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [TxtListIndentation()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [character](./character/) | Gets or sets which character to use for indenting list levels. The default value is '\\0', that means there is no indentation. |
| [count](./count/) | Gets or sets how many [TxtListIndentation.character](./character/) to use as indentation per one list level. The default value is 0, that means no indentation. |

### Examples

Shows how to configure list indenting when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a list with three levels of indentation.
builder.list_format.apply_number_default()
builder.writeln("Item 1")
builder.list_format.list_indent()
builder.writeln("Item 2")
builder.list_format.list_indent()
builder.write("Item 3")

# Create a "TxtSaveOptions" object, which we can pass to the document's "save" method
# to modify how we save the document to plaintext.
txt_save_options = aw.saving.TxtSaveOptions()

# Set the "character" property to assign a character to use
# for padding that simulates list indentation in plaintext.
txt_save_options.list_indentation.character = ' '

# Set the "count" property to specify the number of times
# to place the padding character for each list indent level.
txt_save_options.list_indentation.count = 3

doc.save(ARTIFACTS_DIR + "TxtSaveOptions.txt_list_indentation.txt", txt_save_options)

with open(ARTIFACTS_DIR + "TxtSaveOptions.txt_list_indentation.txt", "rb") as file:
    doc_text = file.read().decode("utf-8-sig")

self.assertEqual(
    "1. Item 1\r\n" +
    "   a. Item 2\r\n" +
    "      i. Item 3\r\n", doc_text)
```

### See Also

* module [aspose.words.saving](../)

