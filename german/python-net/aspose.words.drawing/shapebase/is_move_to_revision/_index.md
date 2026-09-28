---
title: ShapeBase.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 350
url: /de/python-net/aspose.words.drawing/shapebase/is_move_to_revision/
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
# Eine Verschiebungsrevision ist, wenn wir ein Element im Dokumentkörper durch Ausschneiden und Einfügen in Microsoft Word verschieben während
# Änderungen nachverfolgt werden. Wenn wir eine Inline‑Form in eine solche Textverschiebung einbeziehen, wird diese Form ebenfalls eine Revision.
# Kopieren‑ und‑Einfügen oder Verschieben von schwebenden Formen erzeugen keine Verschiebungsrevisionen.
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# Verschiebungsrevisionen bestehen aus Paaren von "Move from"‑ und "Move to"‑Revisionen. Wir haben in diesem Dokument eine Form verschoben,
# aber bis wir die Verschiebungsrevision akzeptieren oder ablehnen, wird es zwei Instanzen dieser Form geben.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Dies ist die "Move to"-Revision, die die Form an ihrem Ankunftsziel ist.
# Wenn wir die Revision akzeptieren, wird diese "Move to"-Revisionsform verschwinden,
# und die "Move from"-Revisionsform bleibt erhalten.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# Dies ist die "Move from"-Revision, die die Form an ihrem ursprünglichen Ort ist.
# Wenn wir die Revision akzeptieren, wird diese "Move from"-Revisionsform verschwinden,
# und die "Move to"-Revisionsform bleibt erhalten.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

