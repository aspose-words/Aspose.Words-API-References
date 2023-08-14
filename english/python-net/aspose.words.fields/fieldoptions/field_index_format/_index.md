---
title: FieldOptions.field_index_format property
linktitle: field_index_format property
articleTitle: field_index_format property
second_title: Aspose.Words for Python
description: "FieldOptions.field_index_format property. Gets or sets a [FieldOptions.field_index_format](./) that represents the formatting for the [FieldIndex](../../fieldindex/) fields in the document."
type: docs
weight: 90
url: /python-net/aspose.words.fields/fieldoptions/field_index_format/
---

## FieldOptions.field_index_format property

Gets or sets a [FieldOptions.field_index_format](./) that represents
the formatting for the [FieldIndex](../../fieldindex/) fields in the document.



### Examples

Shows how to formatting FieldIndex fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write("A")
builder.insert_break(aw.BreakType.LINE_BREAK)
builder.insert_field("XE \"A\"")
builder.write("B")

builder.insert_field(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", None)

doc.field_options.field_index_format = aw.fields.FieldIndexFormat.FANCY
doc.update_fields()

doc.save(ARTIFACTS_DIR + "Field.set_field_index_format.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

