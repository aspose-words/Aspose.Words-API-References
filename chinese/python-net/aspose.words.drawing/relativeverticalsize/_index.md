---
title: RelativeVerticalSize enumeration
linktitle: RelativeVerticalSize enumeration
articleTitle: RelativeVerticalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeVerticalSize enumeration. Specifies relatively to what the height of a shape or a text frame is calculated vertically."
type: docs
weight: 330
url: /zh/python-net/aspose.words.drawing/relativeverticalsize/
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
* property [ShapeBase.relative_vertical_size](../shapebase/relative_vertical_size/)

