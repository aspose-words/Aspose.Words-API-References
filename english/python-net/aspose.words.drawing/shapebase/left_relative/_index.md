---
title: ShapeBase.left_relative property
linktitle: left_relative property
articleTitle: left_relative property
second_title: Aspose.Words for Python
description: "ShapeBase.left_relative property. Gets or sets the value that represents shape's relative left position in percent."
type: docs
weight: 390
url: /python-net/aspose.words.drawing/shapebase/left_relative/
---

## ShapeBase.left_relative property

Gets or sets the value that represents shape's relative left position in percent.


```python
@property
def left_relative(self) -> float:
    ...

@left_relative.setter
def left_relative(self, value: float):
    ...

```

### Examples

Shows how to set relative size and position.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Adding a simple shape with absolute size and position.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
shape.wrap_type = aw.drawing.WrapType.NONE
# Checking and setting the relative horizontal size.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # Setting the horizontal size binding to Margin.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # Setting the width to 50% of Margin width.
    shape.width_relative = 50
# Checking and setting the relative vertical size.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # Setting the vertical size binding to Margin.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # Setting the heigh to 30% of Margin height.
    shape.height_relative = 30
# Checking and setting the relative vertical position.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # etting the position binding to TopMargin.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # Setting relative Top to 30% of TopMargin position.
    shape.top_relative = 30
# Checking and setting the relative horizontal position.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # Setting the position binding to RightMargin.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # The position relative value can be negative.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

