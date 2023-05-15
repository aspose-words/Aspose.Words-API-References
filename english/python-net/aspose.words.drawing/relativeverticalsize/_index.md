---
title: RelativeVerticalSize enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies relatively to what the height of a shape or a text frame is calculated vertically."
type: docs
weight: 290
url: /python-net/aspose.words.drawing/relativeverticalsize/
---

## RelativeVerticalSize enumeration

Specifies relatively to what the height of a shape or a text frame is calculated vertically.


### Members

| Name | Description |
| --- | --- |
| MARGIN | Specifies that the height is calculated relatively to the space between the top and the bottom margins. |
| PAGE | Specifies that the height is calculated relatively to the page height. |
| TOP_MARGIN | Specifies that the height is calculated relatively to the top margin area size. |
| BOTTOM_MARGIN | Specifies that the height is calculated relatively to the bottom margin area size. |
| INNER_MARGIN | Specifies that the height is calculated relatively to the inside margin area size, to the top margin area size for odd pages and to the bottom margin area size for even pages. |
| OUTER_MARGIN | Specifies that the height is calculated relatively to the outside margin area size, to the bottom margin area size for odd pages and to the top margin area size for even pages. |
| DEFAULT | Default value is [RelativeVerticalSize.MARGIN](./#MARGIN). |

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

* module [aspose.words.drawing](../)
* property [ShapeBase.relative_vertical_size](../shapebase/relative_vertical_size/)

