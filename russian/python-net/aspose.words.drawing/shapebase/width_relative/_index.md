---
title: ShapeBase.width_relative property
linktitle: width_relative property
articleTitle: width_relative property
second_title: Aspose.Words for Python
description: "ShapeBase.width_relative property. Gets or sets the value that represents the percentage of shape's relative width."
type: docs
weight: 620
url: /ru/python-net/aspose.words.drawing/shapebase/width_relative/
---

## ShapeBase.width_relative property

Gets or sets the value that represents the percentage of shape's relative width.


```python
@property
def width_relative(self) -> float:
    ...

@width_relative.setter
def width_relative(self, value: float):
    ...

```

### Examples

Shows how to set relative size and position.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Добавление простой фигуры с абсолютным размером и позицией.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# Установите WrapType в значение WrapType.None, так как встроенные (Inline) фигуры автоматически преобразуются в абсолютные единицы.
shape.wrap_type = aw.drawing.WrapType.NONE
# Проверка и установка относительного горизонтального размера.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # Установка привязки горизонтального размера к Margin.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # Установка ширины в 50% от ширины Margin.
    shape.width_relative = 50
# Проверка и установка относительного вертикального размера.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # Установка привязки вертикального размера к Margin.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # Установка высоты в 30% от высоты Margin.
    shape.height_relative = 30
# Проверка и установка относительного вертикального положения.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # Установка привязки положения к TopMargin.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # Установка относительного Top в 30% от позиции TopMargin.
    shape.top_relative = 30
# Проверка и установка относительного горизонтального положения.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # Установка привязки положения к RightMargin.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # Относительное значение положения может быть отрицательным.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

