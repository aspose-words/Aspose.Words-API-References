---
title: FieldChar.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "FieldChar.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldchar/is_dirty/
---

## FieldChar.is_dirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications
made to the document.


### Examples

Shows how to work with a FieldStart node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.format.date_time_format = "dddd, MMMM dd, yyyy"
field.update()

field_start = field.start

self.assertEqual(aw.fields.FieldType.FIELD_DATE, field_start.field_type)
self.assertFalse(field_start.is_dirty)
self.assertFalse(field_start.is_locked)

# Retrieve the facade object which represents the field in the document.
field = field_start.get_field().as_field_date()

self.assertFalse(field.is_locked)
self.assertEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.get_field_code())

# Update the field to show the current date.
field.update()
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldChar](../)

