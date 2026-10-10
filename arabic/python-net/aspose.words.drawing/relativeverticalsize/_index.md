---
title: RelativeVerticalSize enumeration
linktitle: RelativeVerticalSize enumeration
articleTitle: RelativeVerticalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeVerticalSize enumeration. Specifies relatively to what the height of a shape or a text frame is calculated vertically."
type: docs
weight: 330
url: /ar/python-net/aspose.words.drawing/relativeverticalsize/
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
* property [ShapeBase.relative_vertical_size](../shapebase/relative_vertical_size/)

