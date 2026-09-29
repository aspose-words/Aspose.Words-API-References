---
title: ShapeBase.local_to_parent method
linktitle: local_to_parent method
articleTitle: local_to_parent method
second_title: Aspose.Words for Python
description: "ShapeBase.local_to_parent method. Converts a value from the local coordinate space into the coordinate space of the parent shape."
type: docs
weight: 680
url: /it/python-net/aspose.words.drawing/shapebase/local_to_parent/
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
# Inserisci una forma di gruppo e posizionala 100 punti sotto e a destra di
# il punto di origine delle coordinate x e Y del documento.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# Usa il metodo "LocalToParent" per determinare che (0, 0) sulle coordinate interne x e y del gruppo
# si trova su (100, 100) del sistema di coordinate della forma genitore. Il genitore della forma di gruppo è il documento stesso.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# Per impostazione predefinita, il piano di coordinate interno di una forma ha l'angolo in alto a sinistra a (0, 0),
# e l'angolo in basso a destra a (1000, 1000). A causa delle sue dimensioni, la nostra forma di gruppo copre un'area di 500pt x 500pt
# nel piano del documento. Ciò significa che un movimento di 1pt sul piano di coordinate del documento verrà tradotto
# in un movimento di 2pt sul piano di coordinate della forma di gruppo.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Sposta l'origine degli assi x e y della forma di gruppo dall'angolo in alto a sinistra al centro.
# Questo sposterà ulteriormente le coordinate interne del gruppo rispetto a quelle del documento.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Modificare la scala del piano di coordinate influenzerà anche le posizioni relative.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Se desideriamo aggiungere una forma a questo gruppo definendo la sua posizione in base a una posizione nel documento,
# dovremo prima confermare una posizione nella forma di gruppo che corrisponda a quella del documento.
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

