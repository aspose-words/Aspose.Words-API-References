---
title: RelativeVerticalSize enumeration
linktitle: RelativeVerticalSize enumeration
articleTitle: RelativeVerticalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeVerticalSize enumeration. Specifies relatively to what the height of a shape or a text frame is calculated vertically."
type: docs
weight: 330
url: /tr/python-net/aspose.words.drawing/relativeverticalsize/
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
# Mutlak boyut ve konuma sahip basit bir şekil ekleme.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# WrapType'ı WrapType.None olarak ayarla, çünkü satır içi şekiller otomatik olarak mutlak birimlere dönüştürülür.
shape.wrap_type = aw.drawing.WrapType.NONE
# İlgili yatay boyutu kontrol et ve ayarla.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # Yatay boyut bağlamasını Margin'a ayarla.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # Genişliği Margin genişliğinin %50'si olarak ayarla.
    shape.width_relative = 50
# İlgili dikey boyutu kontrol et ve ayarla.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # Dikey boyut bağlamasını Margin'a ayarla.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # Yüksekliği Margin yüksekliğinin %30'u olarak ayarla.
    shape.height_relative = 30
# İlgili dikey konumu kontrol et ve ayarla.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # konum bağlamasını TopMargin'a ayarlama.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # İlgili üst konumu TopMargin konumunun %30'u olarak ayarla.
    shape.top_relative = 30
# İlgili yatay konumu kontrol et ve ayarla.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # Konum bağlamasını RightMargin'a ayarla.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # Konumun ilgili değeri negatif olabilir.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ShapeBase.relative_vertical_size](../shapebase/relative_vertical_size/)

