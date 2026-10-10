---
title: ShapeBase.coord_size property
linktitle: coord_size property
articleTitle: coord_size property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_size property. The width and height of the coordinate space inside the containing block of this shape."
type: docs
weight: 120
url: /sv/python-net/aspose.words.drawing/shapebase/coord_size/
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
# Skapa en gruppform. En gruppform kan visa en samling av underordnade formnoder.
# I Microsoft Word, att klicka inom gruppformens gräns eller på en av gruppformens underordnade former kommer att
# välja alla andra underordnade former inom denna grupp och låta oss skala och flytta alla former på en gång.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# Skapa en 400pt x 400pt gruppform och placera den vid dokumentets flytande formkoordinatursprung.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# Ställ in gruppens interna koordinatplan till 500 x 500pt.
# Det övre vänstra hörnet av gruppen kommer att ha x- och y-koordinaterna (0, 0),
# och det nedre högra hörnet kommer att ha x- och y-koordinaterna (500, 500).
group.coord_size = aspose.pydrawing.Size(500, 500)
# Ställ in koordinaterna för gruppens övre vänstra hörn till (-250, -250).
# Gruppens centrum kommer nu att ha x- och y-koordinatvärdet (0, 0),
# och det nedre högra hörnet kommer att vara på (250, 250).
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# Skapa en rektangel som kommer att visa gränsen för denna gruppform och lägg till den i gruppen.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# När en form är en del av en gruppform kan vi komma åt den som en underordnad nod och sedan modifiera den.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# Skapa en liten röd stjärna och infoga den i gruppen.
# Rikta upp formen med gruppens koordinatursprung, som vi har flyttat till mitten.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# Infoga en rektangel och sedan infoga en något mindre rektangel på samma plats med en bild.
# Nyare former som vi lägger till i gruppen överlappar äldre former. Den ljusblå rektangeln kommer delvis att överlappa den röda stjärnan,
# och sedan kommer formen med bilden att överlappa den ljusblå rektangeln, genom att använda den som en ram.
# Vi kan inte använda egenskaperna "ZOrder" för former för att manipulera deras placering inom en gruppform.
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
# Infoga en textruta i gruppformen. Ställ in egenskapen "Left" så att textrutans högra kant
# rör den högra gränsen av gruppformen. Ställ in egenskapen "Top" så att textrutan sitter utanför
# gränsen av gruppformen, med dess övre storlek linjerad längs gruppformens nedre marginal.
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

