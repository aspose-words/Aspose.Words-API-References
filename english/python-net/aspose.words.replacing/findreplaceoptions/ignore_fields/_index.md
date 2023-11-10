---
title: FindReplaceOptions.ignore_fields property
linktitle: ignore_fields property
articleTitle: ignore_fields property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_fields property. Gets or sets a boolean value indicating either to ignore text inside fields"
type: docs
weight: 80
url: /python-net/aspose.words.replacing/findreplaceoptions/ignore_fields/
---

## FindReplaceOptions.ignore_fields property

Gets or sets a boolean value indicating either to ignore text inside fields.
The default value is ``False``.



```python
@property
def ignore_fields(self) -> bool:
    ...

@ignore_fields.setter
def ignore_fields(self, value: bool):
    ...

```

### Remarks

This option affects whole field (all nodes between
[NodeType.FIELD_START](../../../aspose.words/nodetype/#FIELD_START) and [NodeType.FIELD_END](../../../aspose.words/nodetype/#FIELD_END)).

To ignore only field codes, please use corresponding option [FindReplaceOptions.ignore_field_codes](../ignore_field_codes/).




### Examples

Shows how to ignore text inside fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")
builder.insert_field("QUOTE", "Hello again!")

# We can use a "FindReplaceOptions" object to modify the find-and-replace process.
options = aw.replacing.FindReplaceOptions()

# Set the "ignore_fields" flag to "True" to get the find-and-replace
# operation to ignore text inside fields.
# Set the "ignore_fields" flag to "False" to get the find-and-replace
# operation to also search for text inside fields.
options.ignore_fields = ignore_text_inside_fields

doc.range.replace("Hello", "Greetings", options)

if ignore_text_inside_fields:
    self.assertEqual(
        "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015",
        doc.get_text().strip())
else:
    self.assertEqual(
        "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015",
        doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

