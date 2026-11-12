---
title: ShapeBase.height_relative property
linktitle: height_relative property
articleTitle: height_relative property
second_title: Aspose.Words for Python
description: "ShapeBase.height_relative property. Gets or sets the value that represents the percentage of shape's relative height."
type: docs
weight: 220
url: /tr/python-net/aspose.words.drawing/shapebase/height_relative/
---

## ShapeBase.height_relative property

Gets or sets the value that represents the percentage of shape's relative height.


```python
@property
def height_relative(self) -> float:
    ...

@height_relative.setter
def height_relative(self, value: float):
    ...

```

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

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

