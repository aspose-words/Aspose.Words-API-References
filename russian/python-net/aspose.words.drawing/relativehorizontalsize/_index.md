---
title: RelativeHorizontalSize enumeration
linktitle: RelativeHorizontalSize enumeration
articleTitle: RelativeHorizontalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeHorizontalSize enumeration. Specifies relatively to what the width of a shape or a text frame is calculated horizontally."
type: docs
weight: 310
url: /ru/python-net/aspose.words.drawing/relativehorizontalsize/
---

## RelativeHorizontalSize enumeration

Specifies relatively to what the width of a shape or a text frame is calculated horizontally.


### Members

| Name | Description |
| --- | --- |
| MARGIN | Specifies that the width is calculated relatively to the space between the left and the right margins. |
| PAGE | Specifies that the width is calculated relatively to the page width. |
| LEFT_MARGIN | Specifies that the width is calculated relatively to the left margin area size. |
| RIGHT_MARGIN | Specifies that the width is calculated relatively to the right margin area size. |
| INNER_MARGIN | Specifies that the width is calculated relatively to the inside margin area size, to the left margin area size for odd pages and to the right margin area size for even pages. |
| OUTER_MARGIN | Specifies that the width is calculated relatively to the outside margin area size, to the right margin area size for odd pages and to the left margin area size for even pages. |
| DEFAULT | Default value is [RelativeHorizontalSize.MARGIN](./#MARGIN). |

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

* module [aspose.words.drawing](../)
* property [ShapeBase.relative_horizontal_size](../shapebase/relative_horizontal_size/)

