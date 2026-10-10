---
title: Shape.fill_color property
linktitle: fill_color property
articleTitle: fill_color property
second_title: Aspose.Words for Python
description: "Shape.fill_color property. Defines the brush color that fills the closed path of the shape."
type: docs
weight: 50
url: /ru/python-net/aspose.words.drawing/shape/fill_color/
---

## Shape.fill_color property

Defines the brush color that fills the closed path of the shape.


```python
@property
def fill_color(self) -> aspose.pydrawing.Color:
    ...

@fill_color.setter
def fill_color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

This is a shortcut to the [Fill.color](../../fill/color/) property.

The default value is
aspose.pydrawing.Color.white.





### Examples

Shows how to fill a shape with a solid color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Напишите некоторый текст, а затем закройте его плавающей фигурой.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Используйте свойство "StrokeColor", чтобы задать цвет контура фигуры.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Используйте свойство "FillColor", чтобы задать цвет внутренней области фигуры.
shape.fill_color = aspose.pydrawing.Color.light_blue
# Свойство "Opacity" определяет степень прозрачности цвета по шкале от 0 до 1,
# где 1 — полностью непрозрачный, а 0 — невидимый.
# Заливка фигуры по умолчанию полностью непрозрачна, поэтому мы не видим текст, находящийся под этой фигурой.
self.assertEqual(1, shape.fill.opacity)
# Установите более низкую непрозрачность цвета заливки фигуры, чтобы увидеть текст под ней.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

