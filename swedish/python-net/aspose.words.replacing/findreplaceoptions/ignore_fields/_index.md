---
title: FindReplaceOptions.ignore_fields property
linktitle: ignore_fields property
articleTitle: ignore_fields property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_fields property. Gets or sets a boolean value indicating either to ignore text inside fields"
type: docs
weight: 80
url: /sv/python-net/aspose.words.replacing/findreplaceoptions/ignore_fields/
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
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
builder.insert_field(field_code='QUOTE', field_value='Hello again!')
# Vi kan använda ett \"FindReplaceOptions\"-objekt för att ändra sök‑och‑ersätt‑processen.
options = aw.replacing.FindReplaceOptions()
# Ställ in flaggan "IgnoreFields" till "true" för att få sök‑och‑ersätt
# operationen för att ignorera text i fält.
# Ställ in flaggan "IgnoreFields" till "false" för att få sök‑och‑ersätt
# operationen för att även söka efter text i fält.
options.ignore_fields = ignore_text_inside_fields
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\r\x13QUOTE\x14Hello again!\x15' if ignore_text_inside_fields else 'Greetings world!\r\x13QUOTE\x14Greetings again!\x15', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

