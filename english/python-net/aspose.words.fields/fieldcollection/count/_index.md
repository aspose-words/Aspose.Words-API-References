---
title: FieldCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "FieldCollection.count property. Returns the number of the fields in the collection."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldcollection/count/
---

## FieldCollection.count property

Returns the number of the fields in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to remove fields from a field collection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_field(field_code=' DATE \\@ "dddd, d MMMM yyyy" ')
builder.insert_field(field_code=' TIME ')
builder.insert_field(field_code=' REVNUM ')
builder.insert_field(field_code=' AUTHOR  "John Doe" ')
builder.insert_field(field_code=' SUBJECT "My Subject" ')
builder.insert_field(field_code=' QUOTE "Hello world!" ')
doc.update_fields()
fields = doc.range.fields
self.assertEqual(6, fields.count)
# Below are four ways of removing fields from a field collection.
# 1 -  Get a field to remove itself:
fields[0].remove()
self.assertEqual(5, fields.count)
# 2 -  Get the collection to remove a field that we pass to its removal method:
last_field = fields[3]
fields.remove(last_field)
self.assertEqual(4, fields.count)
# 3 -  Remove a field from a collection at an index:
fields.remove_at(2)
self.assertEqual(3, fields.count)
# 4 -  Remove all the fields from the collection at once:
fields.clear()
self.assertEqual(0, fields.count)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCollection](../)

