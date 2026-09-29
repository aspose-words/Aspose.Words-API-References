---
title: ShapeBase.width_relative property
linktitle: width_relative property
articleTitle: width_relative property
second_title: Aspose.Words for Python
description: "ShapeBase.width_relative property. Gets or sets the value that represents the percentage of shape's relative width."
type: docs
weight: 620
url: /it/python-net/aspose.words.drawing/shapebase/width_relative/
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
# Aggiunta di una forma semplice con dimensione e posizione assolute.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# Imposta WrapType a WrapType.None poiché le forme Inline vengono convertite automaticamente in unità assolute.
shape.wrap_type = aw.drawing.WrapType.NONE
# Verifica e impostazione della dimensione orizzontale relativa.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # Impostazione del vincolo della dimensione orizzontale a Margin.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # Impostazione della larghezza al 50% della larghezza di Margin.
    shape.width_relative = 50
# Verifica e impostazione della dimensione verticale relativa.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # Impostazione del vincolo della dimensione verticale a Margin.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # Impostazione dell'altezza al 30% dell'altezza di Margin.
    shape.height_relative = 30
# Verifica e impostazione della posizione verticale relativa.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # Impostazione del vincolo della posizione a TopMargin.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # Impostazione del Top relativo al 30% della posizione di TopMargin.
    shape.top_relative = 30
# Verifica e impostazione della posizione orizzontale relativa.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # Impostazione del vincolo della posizione a RightMargin.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # Il valore relativo della posizione può essere negativo.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

