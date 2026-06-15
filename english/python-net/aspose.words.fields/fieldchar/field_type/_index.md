---
title: FieldChar.field_type property
linktitle: field_type property
articleTitle: field_type property
second_title: Aspose.Words for Python
description: "FieldChar.field_type property. Returns the type of the field."
type: docs
weight: 10
url: /python-net/aspose.words.fields/fieldchar/field_type/
---

## FieldChar.field_type property

Returns the type of the field.


```python
@property
def field_type(self) -> aspose.words.fields.FieldType:
    ...

```

### Examples

Shows how to work with a FieldStart node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True).as_field_date()
field.format.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
field_start = field.start
assert field_start.field_type == aw.fields.FieldType.FIELD_DATE
assert field_start.is_dirty == False
assert field_start.is_locked == False
# Retrieve the facade object which represents the field in the document.
field = field_start.get_field().as_field_date()
assert field.is_locked == False
assert field.get_field_code() == ' DATE  \\@ "dddd, MMMM dd, yyyy"'
# Update the field to show the current date.
field.update()
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldChar](../)

