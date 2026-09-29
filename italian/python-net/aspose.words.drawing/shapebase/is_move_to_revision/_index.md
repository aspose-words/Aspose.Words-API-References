---
title: ShapeBase.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 350
url: /it/python-net/aspose.words.drawing/shapebase/is_move_to_revision/
---

## ShapeBase.is_move_to_revision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_to_revision(self) -> bool:
    ...

```

### Examples

Shows how to identify move revision shapes.

```python
# Una revisione di spostamento è quando spostiamo un elemento nel corpo del documento tagliandolo e incollandolo in Microsoft Word mentre
# tracciando le modifiche. Se includiamo una forma in linea in tale spostamento di testo, quella forma sarà anche una revisione.
# Copiare-incollare o spostare forme fluttuanti non crea revisioni di spostamento.
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# Le revisioni di spostamento consistono in coppie di revisioni "Move from" e "Move to". Abbiamo spostato in questo documento una forma,
# ma finché non accetteremo o rifiuteremo la revisione di spostamento, ci saranno due istanze di quella forma.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Questa è la revisione "Move to", che è la forma nella sua destinazione di arrivo.
# Se accettiamo la revisione, questa forma di revisione "Move to" scomparirà,
# e la forma di revisione "Move from" rimarrà.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# Questa è la revisione "Move from", che è la forma nella sua posizione originale.
# Se accettiamo la revisione, questa forma di revisione "Move from" scomparirà,
# e la forma di revisione "Move to" rimarrà.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

