---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /de/python-net/aspose.words.drawing/shapebase/bounds/
---

## ShapeBase.bounds property

Gets or sets the location and size of the containing block of the shape.


```python
@property
def bounds(self) -> aspose.pydrawing.RectangleF:
    ...

@bounds.setter
def bounds(self, value: aspose.pydrawing.RectangleF):
    ...

```

### Remarks

Ignores aspect ratio lock upon setting.


For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.




### Examples

Shows how to create and populate a group shape.

```python
doc = aw.Document()
# Erstellen Sie eine Gruppierungsform. Eine Gruppierungsform kann eine Sammlung von untergeordneten Formknoten anzeigen.
# In Microsoft Word führt ein Klick innerhalb der Begrenzung der Gruppierungsform oder auf einer der untergeordneten Formen der Gruppierungsform dazu,
# alle anderen untergeordneten Formen in dieser Gruppe auszuwählen und ermöglicht es uns, alle Formen gleichzeitig zu skalieren und zu verschieben.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# Erstellen Sie eine 400pt x 400pt große Gruppierungsform und platzieren Sie sie am Koordinatenursprung der schwebenden Form im Dokument.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# Setzen Sie die Größe der internen Koordinatenebene der Gruppe auf 500 x 500pt.
# Die obere linke Ecke der Gruppe hat die x‑ und y‑Koordinate (0, 0),
# und die untere rechte Ecke hat die x‑ und y‑Koordinate (500, 500).
group.coord_size = aspose.pydrawing.Size(500, 500)
# Setzen Sie die Koordinaten der oberen linken Ecke der Gruppe auf (-250, -250).
# Das Zentrum der Gruppe hat nun die x‑ und y‑Koordinate (0, 0),
# und die untere rechte Ecke befindet sich bei (250, 250).
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# Erstellen Sie ein Rechteck, das die Begrenzung dieser Gruppierungsform anzeigt, und fügen Sie es der Gruppe hinzu.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# Sobald eine Form Teil einer Gruppierungsform ist, können wir sie als untergeordneten Knoten zugreifen und anschließend ändern.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# Erstellen Sie einen kleinen roten Stern und fügen Sie ihn in die Gruppe ein.
# Richten Sie die Form an dem Koordinatenursprung der Gruppe aus, den wir in die Mitte verschoben haben.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# Fügen Sie ein Rechteck ein und dann ein etwas kleineres Rechteck an derselben Stelle mit einem Bild ein.
# Neuere Formen, die wir zur Gruppe hinzufügen, überlappen ältere Formen. Das hellblaue Rechteck wird den roten Stern teilweise überlappen,
# und dann wird die Form mit dem Bild das hellblaue Rechteck überlappen und es als Rahmen verwenden.
# Wir können die "ZOrder"-Eigenschaften von Formen nicht verwenden, um ihre Anordnung innerhalb einer Gruppierung zu manipulieren.
child3 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child3.width = 250
child3.height = 250
child3.left = -250
child3.top = -250
child3.fill_color = aspose.pydrawing.Color.light_blue
group.append_child(child3)
child4 = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
child4.width = 200
child4.height = 200
child4.left = -225
child4.top = -225
group.append_child(child4)
group.get_child(aw.NodeType.SHAPE, 3, True).as_shape().image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Fügen Sie ein Textfeld in die Gruppierung ein. Setzen Sie die "Left"-Eigenschaft, sodass die rechte Kante des Textfelds
# die rechte Begrenzung der Gruppierung berührt. Setzen Sie die "Top"-Eigenschaft, sodass das Textfeld außerhalb
# der Begrenzung der Gruppierung liegt, wobei seine obere Größe entlang der unteren Marge der Gruppierung ausgerichtet ist.
child5 = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
child5.width = 200
child5.height = 50
child5.left = group.coord_size.width + group.coord_origin.x - 200
child5.top = group.coord_size.height + group.coord_origin.y
group.append_child(child5)
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(group)
builder.move_to(group.get_child(aw.NodeType.SHAPE, 4, True).as_shape().append_child(aw.Paragraph(doc)))
builder.write('Hello world!')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GroupShape.docx')
```

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

