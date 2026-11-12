---
title: ShapeBase.coord_size property
linktitle: coord_size property
articleTitle: coord_size property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_size property. The width and height of the coordinate space inside the containing block of this shape."
type: docs
weight: 120
url: /ru/python-net/aspose.words.drawing/shapebase/coord_size/
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

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```python
doc = aw.Document()
# Вставьте групповую фигуру и разместите её на 100 пунктов ниже и правее
# точки начала координат X и Y документа.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# Используйте метод "LocalToParent", чтобы определить, что (0, 0) во внутренних координатах X и Y группы
# соответствует (100, 100) в системе координат родительской фигуры. Родителем групповой фигуры является сам документ.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# По умолчанию внутренняя координатная плоскость фигуры имеет левый верхний угол в (0, 0),
# а правый нижний угол — в (1000, 1000). Из‑за своего размера наша групповая фигура покрывает область 500pt × 500pt
# в плоскости документа. Это означает, что перемещение на 1pt в координатной плоскости документа будет соответствовать
# перемещению на 2pt в координатной плоскости групповой фигуры.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Переместите начало осей X и Y групповой фигуры из левого верхнего угла в центр.
# Это ещё сильнее сместит внутренние координаты группы относительно координат документа.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Изменение масштаба координатной плоскости также повлияет на относительные положения.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Если мы хотим добавить фигуру в эту группу, определяя её положение на основе положения в документе,
# нам сначала нужно будет определить место в групповой фигуре, которое будет соответствовать месту в документе.
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

