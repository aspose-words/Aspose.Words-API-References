---
title: ShapeBase.local_to_parent method
linktitle: local_to_parent method
articleTitle: local_to_parent method
second_title: Aspose.Words for Python
description: "ShapeBase.local_to_parent method. Converts a value from the local coordinate space into the coordinate space of the parent shape."
type: docs
weight: 680
url: /ru/python-net/aspose.words.drawing/shapebase/local_to_parent/
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

