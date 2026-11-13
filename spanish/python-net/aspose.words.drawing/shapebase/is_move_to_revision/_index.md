---
title: ShapeBase.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 350
url: /es/python-net/aspose.words.drawing/shapebase/is_move_to_revision/
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
# Una revisión de movimiento es cuando movemos un elemento en el cuerpo del documento mediante cortar y pegar en Microsoft Word mientras
# seguimos los cambios. Si involucramos una forma en línea en dicho movimiento de texto, esa forma también será una revisión.
# Copiar y pegar o mover formas flotantes no crean revisiones de movimiento.
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# Las revisiones de movimiento consisten en pares de revisiones "Move from" y "Move to". Movimos en este documento una forma,
# pero hasta que aceptemos o rechacemos la revisión de movimiento, habrá dos instancias de esa forma.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Esta es la revisión "Move to", que es la forma en su destino de llegada.
# Si aceptamos la revisión, esta forma de revisión "Move to" desaparecerá,
# y la forma de revisión "Move from" permanecerá.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# Esta es la revisión "Move from", que es la forma en su ubicación original.
# Si aceptamos la revisión, esta forma de revisión "Move from" desaparecerá,
# y la forma de revisión "Move to" permanecerá.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

