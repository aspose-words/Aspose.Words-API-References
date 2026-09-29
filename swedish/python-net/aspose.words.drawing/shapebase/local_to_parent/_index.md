---
title: ShapeBase.local_to_parent method
linktitle: local_to_parent method
articleTitle: local_to_parent method
second_title: Aspose.Words for Python
description: "ShapeBase.local_to_parent method. Converts a value from the local coordinate space into the coordinate space of the parent shape."
type: docs
weight: 680
url: /sv/python-net/aspose.words.drawing/shapebase/local_to_parent/
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
# Infoga en gruppform och placera den 100 punkter nedanför och till höger om
# dokumentets x- och Y-koordinatuppgångspunkt.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# Använd metoden "LocalToParent" för att bestämma att (0, 0) på gruppens interna x- och y-koordinater
# ligger på (100, 100) i dess föräldraforms koordinatsystem. Gruppformens förälder är själva dokumentet.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# Som standard har en forms interna koordinatplan det övre vänstra hörnet vid (0, 0),
# och det nedre högra hörnet vid (1000, 1000). På grund av dess storlek täcker vår gruppform ett område på 500pt x 500pt
# i dokumentets plan. Detta betyder att en rörelse på 1pt i dokumentets koordinatplan kommer att översättas
# till en rörelse på 2pt i gruppformens koordinatplan.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Flytta gruppformens x- och y-axelursprung från det övre vänstra hörnet till mitten.
# Detta kommer att förskjuta gruppens interna koordinater i förhållande till dokumentets koordinater ännu mer.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Att ändra skalan på koordinatplanet kommer också att påverka relativa positioner.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Om vi vill lägga till en form i den här gruppen samtidigt som vi definierar dess placering baserat på en plats i dokumentet,
# måste vi först bekräfta en plats i gruppformen som matchar dokumentets plats.
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

