---
title: FieldChar.is_locked property
linktitle: is_locked property
articleTitle: is_locked property
second_title: Aspose.Words for Python
description: "FieldChar.is_locked property. Gets or sets whether the parent field is locked (should not recalculate its result)."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldchar/is_locked/
---

## FieldChar.is_locked property

Gets or sets whether the parent field is locked (should not recalculate its result).


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

