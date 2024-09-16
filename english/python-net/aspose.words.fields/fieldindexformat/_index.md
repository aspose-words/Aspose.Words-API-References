---
title: FieldIndexFormat enumeration
linktitle: FieldIndexFormat enumeration
articleTitle: FieldIndexFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldIndexFormat enumeration. Specifies the formatting for the [FieldIndex](../fieldindex/) fields in a document."
type: docs
weight: 610
url: /python-net/aspose.words.fields/fieldindexformat/
---

## FieldIndexFormat enumeration

Specifies the formatting for the [FieldIndex](../fieldindex/) fields in a document.



### Members

| Name | Description |
| --- | --- |
| TEMPLATE | From template. |
| CLASSIC | Classic. |
| FANCY | Fancy. |
| MODERN | Modern. |
| BULLETED | Bulleted. |
| FORMAL | Formal. |
| SIMPLE | Simple. |

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

* module [aspose.words.fields](../)

