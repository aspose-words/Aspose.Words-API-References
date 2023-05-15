---
title: left_relative property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the value that represents shape's relative left position in percent."
type: docs
weight: 380
url: /python-net/aspose.words.drawing/shapebase/left_relative/
---

## ShapeBase.left_relative property

Gets or sets the value that represents shape's relative left position in percent.


### Examples

Shows how to set relative size and position.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Adding a simple shape with absolute size and position.
shape = builder.insert_shape(awd.ShapeType.RECTANGLE, 100.0, 40.0)

# Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
shape.wrap_type = awd.WrapType.NONE

# Checking and setting the relative horizontal size.
if shape.relative_horizontal_size == awd.RelativeHorizontalSize.DEFAULT:
    # Setting the horizontal size binding to Margin.
    shape.relative_horizontal_size = awd.RelativeHorizontalSize.MARGIN
    # Setting the width to 50 % of Margin width.
    shape.width_relative = 50

# Checking and setting the relative vertical size.
if shape.relative_vertical_size == awd.RelativeVerticalSize.DEFAULT:
    # Setting the vertical size binding to Margin.
    shape.relative_vertical_size = awd.RelativeVerticalSize.MARGIN
    # Setting the height to 30 % of Margin height.
    shape.height_relative = 30

#  Checking and setting the relative vertical position.
if shape.relative_vertical_position == awd.RelativeVerticalPosition.PARAGRAPH:
    # Setting the position binding to TopMargin.
    shape.relative_vertical_position = awd.RelativeVerticalPosition.TOP_MARGIN
    # Setting relative Top to 30 % of TopMargin position.
    shape.top_relative = 30

# Checking and setting the relative horizontal position.
if shape.relative_horizontal_position == awd.RelativeHorizontalPosition.DEFAULT:
    # Setting the position binding to RightMargin.
    shape.relative_horizontal_position = awd.RelativeHorizontalPosition.RIGHT_MARGIN
    # The position relative value can be negative.
    shape.left_relative = -260

doc.save(ARTIFACTS_DIR + "Shape.RelativeSizeAndPosition.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

