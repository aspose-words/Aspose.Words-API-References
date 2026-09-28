---
title: ShapeBase.bounds_in_points property
linktitle: bounds_in_points property
articleTitle: bounds_in_points property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_in_points property. Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape."
type: docs
weight: 80
url: /de/python-net/aspose.words.drawing/shapebase/bounds_in_points/
---

## ShapeBase.bounds_in_points property

Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.


```python
@property
def bounds_in_points(self) -> aspose.pydrawing.RectangleF:
    ...

```

### Remarks

The returned bounds do not include the rotation of this shape or the rotation of the parent group shape, if any.


### Examples

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.LINE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=50, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.stroke_color = aspose.pydrawing.Color.orange
# Obwohl die Linie selbst nur wenig Platz auf der Dokumentenseite einnimmt,
# belegt sie einen rechteckigen Containerblock, dessen Größe wir mit den "Bounds"-Eigenschaften bestimmen können.
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# Erstellen Sie eine Gruppierung und setzen Sie anschließend die Größe ihres Containerblocks mit der "Bounds"-Eigenschaft.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# Erstellen Sie ein Rechteck, überprüfen Sie die Größe seines Begrenzungsblocks und fügen Sie es dann der Gruppierung hinzu.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# Die Koordinatenebene der Gruppierung hat ihren Ursprung in der oberen linken Ecke ihres Containerblocks,
# und die x- und y-Koordinaten von (1000, 1000) in der unteren rechten Ecke.
# Unsere Gruppierung ist 250 × 250 pt groß, sodass alle 4 pt auf der Koordinatenebene der Gruppierung
# entsprechen 1 pt im Koordinatensystem des Dokumentkörpers.
# Jede Form, die wir einfügen, wird ebenfalls um den Faktor 4 verkleinert.
# Die Änderung der "BoundsInPoints"-Eigenschaft der Form wird dies widerspiegeln.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# Fügen Sie eine Form ein und platzieren Sie sie außerhalb der Grenzen des Containerblocks der Gruppierung.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# Der Fußabdruck der Gruppierung im Dokumentkörper hat zugenommen, aber der Containerblock bleibt unverändert.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

