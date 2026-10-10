---
title: ShapeBase.is_delete_revision property
linktitle: is_delete_revision property
articleTitle: is_delete_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_delete_revision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 270
url: /it/python-net/aspose.words.drawing/shapebase/is_delete_revision/
---

## ShapeBase.is_delete_revision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.


```python
@property
def is_delete_revision(self) -> bool:
    ...

```

### Examples

Shows how to work with revision shapes.

```python
doc = aw.Document()
self.assertFalse(doc.track_revisions)
# Inserisci una forma inline senza tenere traccia delle revisioni, il che farà sì che questa forma non sia una revisione di alcun tipo.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# Inizia a tenere traccia delle revisioni e poi inserisci un'altra forma, che sarà una revisione.
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# Poiché abbiamo rimosso quella forma mentre stavamo tracciando le modifiche,
# la forma persiste nel documento e conta come una revisione di eliminazione.
# Accettare questa revisione rimuoverà la forma definitivamente, e rifiutarla la manterrà nel documento.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# E abbiamo inserito un'altra forma mentre tracciavamo le modifiche, quindi quella forma conterà come una revisione di inserimento.
# Accettare questa revisione assimilerà questa forma nel documento come una non-revisione,
# e rifiutare la revisione rimuoverà permanentemente questa forma.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

