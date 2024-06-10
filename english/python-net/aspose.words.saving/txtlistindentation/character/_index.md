---
title: TxtListIndentation.character property
linktitle: character property
articleTitle: character property
second_title: Aspose.Words for Python
description: "TxtListIndentation.character property. Gets or sets which character to use for indenting list levels"
type: docs
weight: 20
url: /python-net/aspose.words.saving/txtlistindentation/character/
---

## TxtListIndentation.character property

Gets or sets which character to use for indenting list levels.
The default value is '\\0', that means there is no indentation.


```python
@property
def character(self) -> str:
    ...

@character.setter
def character(self, value: str):
    ...

```

### Examples

Shows how to configure list indenting when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Create a list with three levels of indentation.
builder.list_format.apply_number_default()
builder.writeln('Item 1')
builder.list_format.list_indent()
builder.writeln('Item 2')
builder.list_format.list_indent()
builder.write('Item 3')
# Create a "TxtSaveOptions" object, which we can pass to the document's "save" method
# to modify how we save the document to plaintext.
txt_save_options = aw.saving.TxtSaveOptions()
# Set the "character" property to assign a character to use
# for padding that simulates list indentation in plaintext.
txt_save_options.list_indentation.character = ' '
# Set the "count" property to specify the number of times
# to place the padding character for each list indent level.
txt_save_options.list_indentation.count = 3
doc.save(ARTIFACTS_DIR + 'TxtSaveOptions.txt_list_indentation.txt', txt_save_options)
with open(ARTIFACTS_DIR + 'TxtSaveOptions.txt_list_indentation.txt', 'rb') as file:
    doc_text = file.read().decode('utf-8-sig')
self.assertEqual('1. Item 1\r\n' + '   a. Item 2\r\n' + '      i. Item 3\r\n', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtListIndentation](../)

