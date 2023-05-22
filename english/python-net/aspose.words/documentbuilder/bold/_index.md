---
title: DocumentBuilder.bold property
linktitle: bold property
articleTitle: bold property
second_title: Aspose.Words for Python
description: "DocumentBuilder.bold property. True if the font is formatted as bold."
type: docs
weight: 20
url: /python-net/aspose.words/documentbuilder/bold/
---

## DocumentBuilder.bold property

True if the font is formatted as bold.


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

