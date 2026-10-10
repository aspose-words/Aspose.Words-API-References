---
title: ShapeBase.bounds_in_points property
linktitle: bounds_in_points property
articleTitle: bounds_in_points property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_in_points property. Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape."
type: docs
weight: 80
url: /ru/python-net/aspose.words.drawing/shapebase/bounds_in_points/
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

