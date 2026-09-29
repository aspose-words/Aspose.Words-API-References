---
title: Field.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "Field.remove method. Removes the field from the document"
type: docs
weight: 1070
url: /es/python-net/aspose.words.fields/field/remove/
---

## remove() {#default}

Removes the field from the document. Returns a node right after the field. If the field's end is the last child
of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.



```python
def remove(self):
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
# A continuación se presentan cuatro formas de eliminar campos de una colección de campos.
# 1 -  Haga que un campo se elimine a sí mismo:
fields[0].remove()
self.assertEqual(5, fields.count)
# 2 -  Haga que la colección elimine un campo que pasamos a su método de eliminación:
last_field = fields[3]
fields.remove(last_field)
self.assertEqual(4, fields.count)
# 3 -  Elimine un campo de una colección en un índice:
fields.remove_at(2)
self.assertEqual(3, fields.count)
# 4 -  Elimine todos los campos de la colección de una vez:
fields.clear()
self.assertEqual(0, fields.count)
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

