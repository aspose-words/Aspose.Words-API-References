---
title: RelativeHorizontalSize enumeration
linktitle: RelativeHorizontalSize enumeration
articleTitle: RelativeHorizontalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeHorizontalSize enumeration. Specifies relatively to what the width of a shape or a text frame is calculated horizontally."
type: docs
weight: 310
url: /ar/python-net/aspose.words.drawing/relativehorizontalsize/
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
# إضافة شكل بسيط بحجم وموقع مطلق.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# عيّن WrapType إلى WrapType.None لأن الأشكال المضمنة تتحول تلقائيًا إلى وحدات مطلقة.
shape.wrap_type = aw.drawing.WrapType.NONE
# التحقق وتعيين الحجم الأفقي النسبي.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # تعيين ربط الحجم الأفقي إلى Margin.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # تعيين العرض إلى 50٪ من عرض Margin.
    shape.width_relative = 50
# التحقق وتعيين الحجم الرأسي النسبي.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # تعيين ربط الحجم الرأسي إلى Margin.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # تعيين الارتفاع إلى 30٪ من ارتفاع Margin.
    shape.height_relative = 30
# التحقق وتعيين الموقع الرأسي النسبي.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # تعيين ربط الموقع إلى TopMargin.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # تعيين Top إلى 30٪ من موقع TopMargin.
    shape.top_relative = 30
# التحقق وتعيين الموقع الأفقي النسبي.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # تعيين ربط الموقع إلى RightMargin.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # القيمة النسبية للموقع يمكن أن تكون سلبية.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ShapeBase.relative_horizontal_size](../shapebase/relative_horizontal_size/)

