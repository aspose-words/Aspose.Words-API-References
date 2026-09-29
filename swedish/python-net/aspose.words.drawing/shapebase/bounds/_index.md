---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /sv/python-net/aspose.words.drawing/shapebase/bounds/
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

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.LINE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=50, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.stroke_color = aspose.pydrawing.Color.orange
# Även om linjen själv tar upp lite utrymme på dokumentets sida,
# den upptar ett rektangulärt innehållsblock, vars storlek vi kan bestämma med hjälp av egenskaperna "Bounds".
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# Skapa en gruppform och sedan ställ in storleken på dess innehållsblock med egenskapen "Bounds".
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# Skapa en rektangel, verifiera storleken på dess omgivande block och lägg sedan till den i gruppformen.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# Gruppformens koordinatplan har sitt ursprung i det övre vänstra hörnet av dess innehållsblock,
# och x- och y-koordinaterna (1000, 1000) i det nedre högra hörnet.
# Vår gruppform är 250×250pt i storlek, så varje 4pt på gruppformens koordinatplan
# översätts till 1pt i dokumentkroppens koordinatplan.
# Varje form som vi infogar kommer också att krympa i storlek med en faktor på 4.
# Ändringen i formens egenskap "BoundsInPoints" kommer att återspegla detta.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# Infoga en form och placera den utanför gränserna för gruppformens innehållsblock.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# Gruppformens fotavtryck i dokumentkroppen har ökat, men innehållsblocket förblir detsamma.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

