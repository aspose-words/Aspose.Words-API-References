---
title: ShapeBase.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 340
url: /sv/python-net/aspose.words.drawing/shapebase/is_move_from_revision/
---

## ShapeBase.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to identify move revision shapes.

```python
# En flyttrevision är när vi flyttar ett element i dokumentkroppen genom att klippa och klistra in det i Microsoft Word medan
# spårar ändringar. Om vi involverar en inline-form i en sådan textflyttning kommer den formen också att vara en revision.
# Kopiera‑och‑klistra eller flytta svävande former skapar inte flyttrevisioner.
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# Flyttrevisioner består av par av "Move from"- och "Move to"-revisioner. Vi flyttade i detta dokument i en form,
# men tills vi accepterar eller avvisar flyttrevisionen kommer det att finnas två instanser av den formen.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Det här är "Move to"-revisionen, som är formen vid dess ankomstdestination.
# Om vi accepterar revisionen kommer den här "Move to"-revisionsformen att försvinna,
# och den "Move from"-revisionsformen kommer att finnas kvar.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# Det här är "Move from"-revisionen, som är formen på dess ursprungliga plats.
# Om vi accepterar revisionen kommer den här "Move from"-revisionsformen att försvinna,
# och den "Move to"-revisionsformen kommer att finnas kvar.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

