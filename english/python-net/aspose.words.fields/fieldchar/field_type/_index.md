---
title: field_type property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns the type of the field."
type: docs
weight: 10
url: /python-net/aspose.words.fields/fieldchar/field_type/
---

## FieldChar.field_type property

Returns the type of the field.


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

