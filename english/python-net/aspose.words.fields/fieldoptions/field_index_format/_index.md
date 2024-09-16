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



```python
@property
def field_index_format(self) -> aspose.words.fields.FieldIndexFormat:
    ...

@field_index_format.setter
def field_index_format(self, value: aspose.words.fields.FieldIndexFormat):
    ...

```

### Examples

Shows how to formatting FieldIndex fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('A')
builder.insert_break(aw.BreakType.LINE_BREAK)
builder.insert_field(field_code='XE "A"')
builder.write('B')
builder.insert_field(field_code=' INDEX \\e " · " \\h "A" \\c "2" \\z "1033"', field_value=None)
doc.field_options.field_index_format = aw.fields.FieldIndexFormat.FANCY
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SetFieldIndexFormat.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

