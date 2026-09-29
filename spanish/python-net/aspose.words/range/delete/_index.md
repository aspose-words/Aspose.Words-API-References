---
title: Range.delete method
linktitle: delete method
articleTitle: delete method
second_title: Aspose.Words for Python
description: "Range.delete method. Deletes all characters of the range."
type: docs
weight: 70
url: /es/python-net/aspose.words/range/delete/
---

## delete() {#default}

Deletes all characters of the range.


```python
def delete(self):
    ...
```

### Examples

Shows how to delete all the nodes from a range.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Agregue texto a la primera sección del documento y luego añada otra sección.
builder.write('Section 1. ')
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.write('Section 2.')
self.assertEqual('Section 1. \x0cSection 2.', doc.get_text().strip())
# Elimine la primera sección por completo eliminando todos los nodos
# dentro de su rango, incluida la propia sección.
doc.sections[0].range.delete()
self.assertEqual(1, doc.sections.count)
self.assertEqual('Section 2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Range](../)

