---
title: RelativeHorizontalSize enumeration
linktitle: RelativeHorizontalSize enumeration
articleTitle: RelativeHorizontalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeHorizontalSize enumeration. Specifies relatively to what the width of a shape or a text frame is calculated horizontally."
type: docs
weight: 310
url: /zh/python-net/aspose.words.drawing/relativehorizontalsize/
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
# 添加具有绝对大小和位置的简单形状。
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# 将 WrapType 设置为 WrapType.None，因为内联形状会自动转换为绝对单位。
shape.wrap_type = aw.drawing.WrapType.NONE
# 检查并设置相对水平尺寸。
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # 将水平尺寸绑定设置为 Margin。
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # 将宽度设置为 Margin 宽度的 50%。
    shape.width_relative = 50
# 检查并设置相对垂直尺寸。
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # 将垂直尺寸绑定设置为 Margin。
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # 将高度设置为 Margin 高度的 30%。
    shape.height_relative = 30
# 检查并设置相对垂直位置。
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # 将位置绑定设置为 TopMargin。
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # 将相对顶部设置为 TopMargin 位置的 30%。
    shape.top_relative = 30
# 检查并设置相对水平位置。
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # 将位置绑定设置为 RightMargin。
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # 相对位置值可以为负。
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ShapeBase.relative_horizontal_size](../shapebase/relative_horizontal_size/)

