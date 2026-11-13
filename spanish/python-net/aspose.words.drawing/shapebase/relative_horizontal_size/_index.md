---
title: ShapeBase.relative_horizontal_size property
linktitle: relative_horizontal_size property
articleTitle: relative_horizontal_size property
second_title: Aspose.Words for Python
description: "ShapeBase.relative_horizontal_size property. Gets or sets the value of shape's relative size in horizontal direction."
type: docs
weight: 460
url: /es/python-net/aspose.words.drawing/shapebase/relative_horizontal_size/
---

## ShapeBase.relative_horizontal_size property

Gets or sets the value of shape's relative size in horizontal direction.


```python
@property
def relative_horizontal_size(self) -> aspose.words.drawing.RelativeHorizontalSize:
    ...

@relative_horizontal_size.setter
def relative_horizontal_size(self, value: aspose.words.drawing.RelativeHorizontalSize):
    ...

```

### Remarks

The default value is [RelativeHorizontalSize](../../relativehorizontalsize/).

Has effect only if [ShapeBase.width_relative](../width_relative/) is set.




### Examples

Shows how to set relative size and position.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Agregar una forma simple con tamaño y posición absolutos.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# Establezca WrapType a WrapType.None ya que las formas Inline se convierten automáticamente a unidades absolutas.
shape.wrap_type = aw.drawing.WrapType.NONE
# Comprobando y estableciendo el tamaño horizontal relativo.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # Estableciendo la vinculación del tamaño horizontal a Margin.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # Estableciendo el ancho al 50% del ancho de Margin.
    shape.width_relative = 50
# Comprobando y estableciendo el tamaño vertical relativo.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # Estableciendo la vinculación del tamaño vertical a Margin.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # Estableciendo la altura al 30% de la altura de Margin.
    shape.height_relative = 30
# Comprobando y estableciendo la posición vertical relativa.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # Estableciendo la vinculación de posición a TopMargin.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # Estableciendo Top relativo al 30% de la posición de TopMargin.
    shape.top_relative = 30
# Comprobando y estableciendo la posición horizontal relativa.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # Estableciendo la vinculación de posición a RightMargin.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # El valor relativo de la posición puede ser negativo.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

