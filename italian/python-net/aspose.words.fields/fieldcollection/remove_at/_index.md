---
title: FieldCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "FieldCollection.remove_at method. Removes a field at the specified index from this collection and from the document."
type: docs
weight: 50
url: /it/python-net/aspose.words.fields/fieldcollection/remove_at/
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
# Di seguito sono riportati quattro modi per rimuovere i campi da una collezione di campi.
# 1 -  Fai in modo che un campo si rimuova da solo:
fields[0].remove()
self.assertEqual(5, fields.count)
# 2 -  Fai in modo che la collezione rimuova un campo che passiamo al suo metodo di rimozione:
last_field = fields[3]
fields.remove(last_field)
self.assertEqual(4, fields.count)
# 3 -  Rimuovi un campo da una collezione a un indice:
fields.remove_at(2)
self.assertEqual(3, fields.count)
# 4 -  Rimuovi tutti i campi dalla collezione in una volta:
fields.clear()
self.assertEqual(0, fields.count)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCollection](../)

