---
title: DocumentBuilder.italic property
linktitle: italic property
articleTitle: italic property
second_title: Aspose.Words for Python
description: "DocumentBuilder.italic property. True if the font is formatted as italic."
type: docs
weight: 140
url: /python-net/aspose.words/documentbuilder/italic/
---

## DocumentBuilder.italic property

True if the font is formatted as italic.


```python
@property
def italic(self) -> bool:
    ...

@italic.setter
def italic(self, value: bool):
    ...

```

### Examples

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
# and then fill them manually.
builder.insert_field(" MERGEFIELD Chairman ")
builder.insert_field(" MERGEFIELD ChiefFinancialOfficer ")
builder.insert_field(" MERGEFIELD ChiefTechnologyOfficer ")

builder.move_to_merge_field("Chairman")
builder.bold = True
builder.writeln("John Doe")

builder.move_to_merge_field("ChiefFinancialOfficer")
builder.italic = True
builder.writeln("Jane Doe")

builder.move_to_merge_field("ChiefTechnologyOfficer")
builder.italic = True
builder.writeln("John Bloggs")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.fill_merge_fields.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

