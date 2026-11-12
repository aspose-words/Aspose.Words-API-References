---
title: FieldCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "FieldCollection.remove_at method. Removes a field at the specified index from this collection and from the document."
type: docs
weight: 50
url: /ru/python-net/aspose.words.fields/fieldcollection/remove_at/
---

## remove_at(index) {#int}

Removes a field at the specified index from this collection and from the document.


```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

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
# Ниже представлены четыре способа удаления полей из коллекции полей.
# 1 -  Получить поле, которое удалит само себя:
fields[0].remove()
self.assertEqual(5, fields.count)
# 2 -  Получить коллекцию, чтобы удалить поле, которое мы передаём её методу удаления:
last_field = fields[3]
fields.remove(last_field)
self.assertEqual(4, fields.count)
# 3 -  Удалить поле из коллекции по индексу:
fields.remove_at(2)
self.assertEqual(3, fields.count)
# 4 -  Удалить все поля из коллекции сразу:
fields.clear()
self.assertEqual(0, fields.count)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCollection](../)

