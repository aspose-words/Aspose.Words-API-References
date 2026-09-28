---
title: ShapeBase.coord_size property
linktitle: coord_size property
articleTitle: coord_size property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_size property. The width and height of the coordinate space inside the containing block of this shape."
type: docs
weight: 120
url: /de/python-net/aspose.words.drawing/shapebase/coord_size/
---

## ShapeBase.coord_size property

The width and height of the coordinate space inside the containing block of this shape.


```python
@property
def coord_size(self) -> aspose.pydrawing.Size:
    ...

@coord_size.setter
def coord_size(self, value: aspose.pydrawing.Size):
    ...

```

### Remarks

The default value is (1000, 1000).




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

