---
title: ShapeBase.local_to_parent method
linktitle: local_to_parent method
articleTitle: local_to_parent method
second_title: Aspose.Words for Python
description: "ShapeBase.local_to_parent method. Converts a value from the local coordinate space into the coordinate space of the parent shape."
type: docs
weight: 680
url: /de/python-net/aspose.words.drawing/shapebase/local_to_parent/
---

## local_to_parent(value) {#pointf}

Converts a value from the local coordinate space into the coordinate space of the parent shape.


```python
def local_to_parent(self, value: aspose.pydrawing.PointF):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | aspose.pydrawing.PointF |  |

### Examples

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```python
doc = aw.Document()
# Fügen Sie eine Gruppierungsform ein und platzieren Sie sie 100 Punkte unterhalb und rechts von
# dem Ursprungspunkt der x‑ und Y‑Koordinaten des Dokuments.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# Verwenden Sie die "LocalToParent"‑Methode, um zu bestimmen, dass (0, 0) auf den internen x‑ und y‑Koordinaten der Gruppe liegt
# liegt bei (100, 100) im Koordinatensystem der übergeordneten Form. Der Elternteil der Gruppierungsform ist das Dokument selbst.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# Standardmäßig hat die interne Koordinatenebene einer Form die obere linke Ecke bei (0, 0),
# und die untere rechte Ecke bei (1000, 1000). Aufgrund ihrer Größe deckt unsere Gruppierungsform einen Bereich von 500pt x 500pt ab
# in der Ebene des Dokuments. Das bedeutet, dass eine Bewegung von 1pt in der Koordinatenebene des Dokuments übersetzt wird
# zu einer Bewegung von 2pt in der Koordinatenebene der Gruppierungsform.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Verschieben Sie den Ursprung der x‑ und y‑Achse der Gruppierungsform von der oberen linken Ecke zum Mittelpunkt.
# Dies wird die internen Koordinaten der Gruppe relativ zu den Koordinaten des Dokuments noch weiter verschieben.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Das Ändern der Skalierung der Koordinatenebene wirkt sich ebenfalls auf relative Positionen aus.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Wenn wir einer Gruppe eine Form hinzufügen möchten, während wir ihre Position basierend auf einer Position im Dokument festlegen,
# müssen wir zunächst einen Ort in der Gruppierungsform bestätigen, der mit der Position im Dokument übereinstimmt.
self.assertEqual(aspose.pydrawing.PointF(700, 700), group.local_to_parent(aspose.pydrawing.PointF(350, 350)))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
group.append_child(shape)
doc.first_section.body.first_paragraph.append_child(group)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.LocalToParent.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

