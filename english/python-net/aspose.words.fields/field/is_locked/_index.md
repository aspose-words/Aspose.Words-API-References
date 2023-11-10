---
title: Field.is_locked property
linktitle: is_locked property
articleTitle: is_locked property
second_title: Aspose.Words for Python
description: "Field.is_locked property. Gets or sets whether the field is locked (should not recalculate its result)."
type: docs
weight: 50
url: /python-net/aspose.words.fields/field/is_locked/
---

## Field.is_locked property

Gets or sets whether the field is locked (should not recalculate its result).


```python
@property
def is_locked(self) -> bool:
    ...

@is_locked.setter
def is_locked(self, value: bool):
    ...

```

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
* class [Field](../)

