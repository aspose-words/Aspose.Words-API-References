---
title: ShapeBase.distance_bottom property
linktitle: distance_bottom property
articleTitle: distance_bottom property
second_title: Aspose.Words for Python
description: "ShapeBase.distance_bottom property. Returns or sets the distance (in points) between the document text and the bottom edge of the shape."
type: docs
weight: 130
url: /ru/python-net/aspose.words.drawing/shapebase/distance_bottom/
---

## ShapeBase.distance_bottom property

Returns or sets the distance (in points) between the document text and the bottom edge of the shape.


```python
@property
def distance_bottom(self) -> float:
    ...

@distance_bottom.setter
def distance_bottom(self, value: float):
    ...

```

### Remarks

The default value is 0.

Has effect only for top level shapes.




### Examples

Shows how to set the wrapping distance for a text that surrounds a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте прямоугольник и заставьте текст плотно обтекать его границы.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=150, height=150)
shape.wrap_type = aw.drawing.WrapType.TIGHT
# Установите минимальное расстояние между фигурой и окружающим текстом в 40pt со всех сторон.
shape.distance_top = 40
shape.distance_bottom = 40
shape.distance_left = 40
shape.distance_right = 40
# Переместите фигуру ближе к центру страницы, а затем поверните её на 60 градусов по часовой стрелке.
shape.top = 75
shape.left = 150
shape.rotation = 60
# Добавьте текст, который будет обтекать фигуру.
builder.font.size = 24
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Coordinates.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

