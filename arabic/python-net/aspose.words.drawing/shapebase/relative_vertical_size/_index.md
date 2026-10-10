---
title: ShapeBase.relative_vertical_size property
linktitle: relative_vertical_size property
articleTitle: relative_vertical_size property
second_title: Aspose.Words for Python
description: "ShapeBase.relative_vertical_size property. Gets or sets the value of shape's relative size in vertical direction."
type: docs
weight: 480
url: /ar/python-net/aspose.words.drawing/shapebase/relative_vertical_size/
---

## ShapeBase.relative_vertical_size property

Gets or sets the value of shape's relative size in vertical direction.


```python
@property
def relative_vertical_size(self) -> aspose.words.drawing.RelativeVerticalSize:
    ...

@relative_vertical_size.setter
def relative_vertical_size(self, value: aspose.words.drawing.RelativeVerticalSize):
    ...

```

### Remarks

The default value is [RelativeVerticalSize.MARGIN](../../relativeverticalsize/#MARGIN).

Has effect only if [ShapeBase.height_relative](../height_relative/) is set.




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

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

