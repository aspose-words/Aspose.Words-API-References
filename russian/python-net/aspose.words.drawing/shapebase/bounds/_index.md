---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /ru/python-net/aspose.words.drawing/shapebase/bounds/
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
# Создайте групповую форму. Групповая форма может отображать коллекцию дочерних узлов формы.
# В Microsoft Word щелчок внутри границы групповой формы или по одной из её дочерних форм будет
# выбирать все остальные дочерние формы внутри этой группы и позволять нам масштабировать и перемещать все формы одновременно.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# Создайте групповую форму размером 400pt x 400pt и разместите её в начале координат плавающей формы документа.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# Установите размер внутренней координатной плоскости группы в 500 x 500pt.
# Верхний левый угол группы будет иметь координаты x и y (0, 0),
# а нижний правый угол будет иметь координаты x и y (500, 500).
group.coord_size = aspose.pydrawing.Size(500, 500)
# Установите координаты верхнего левого угла группы в (-250, -250).
# Центр группы теперь будет иметь координаты x и y (0, 0),
# а нижний правый угол будет находиться в (250, 250).
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# Создайте прямоугольник, который будет отображать границу этой групповой формы, и добавьте его в группу.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# После того как форма станет частью групповой формы, мы можем получить к ней доступ как к дочернему узлу и затем изменить её.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# Создайте небольшую красную звезду и вставьте её в группу.
# Выровняйте фигуру с началом координат группы, которое мы переместили в центр.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# Вставьте прямоугольник, а затем вставьте чуть меньший прямоугольник в том же месте с изображением.
# Новые фигуры, которые мы добавляем в группу, перекрывают более старые фигуры. Светло‑голубой прямоугольник будет частично перекрывать красную звезду,
# а затем фигура с изображением перекроет светло‑голубой прямоугольник, используя его в качестве рамки.
# Мы не можем использовать свойства "ZOrder" фигур для управления их расположением внутри групповой фигуры.
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
# Вставьте текстовое поле в групповую фигуру. Установите свойство "Left", чтобы правая граница текстового поля
# касалась правой границы групповой фигуры. Установите свойство "Top", чтобы текстовое поле находилось за пределами
# границы групповой фигуры, при этом верхний размер будет выровнен по нижнему полю групповой фигуры.
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
# Несмотря на то, что сама линия занимает мало места на странице документа,
# она занимает прямоугольный блок‑контейнер, размер которого мы можем определить с помощью свойств "Bounds".
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# Создайте групповую фигуру, а затем задайте размер её блока‑контейнера, используя свойство "Bounds".
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# Создайте прямоугольник, проверьте размер его ограничивающего блока и затем добавьте его в групповую фигуру.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# Плоскость координат групповой фигуры имеет начало в верхнем левом углу её блока‑контейнера,
# а координаты x и y (1000, 1000) находятся в нижнем правом углу.
# Наша групповая фигура имеет размер 250×250pt, поэтому каждый 4pt на её плоскости координат
# соответствует 1pt в плоскости координат тела документа.
# Каждая вставляемая фигура также уменьшится в размере в 4 раза.
# Изменение свойства "BoundsInPoints" фигуры будет отражать это.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# Вставьте фигуру и разместите её за пределами границ блока‑контейнера групповой фигуры.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# Отпечаток групповой фигуры в теле документа увеличился, но блок‑контейнер остался прежним.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

