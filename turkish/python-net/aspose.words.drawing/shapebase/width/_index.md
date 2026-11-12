---
title: ShapeBase.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "ShapeBase.width property. Gets or sets the width of the containing block of the shape."
type: docs
weight: 610
url: /tr/python-net/aspose.words.drawing/shapebase/width/
---

## ShapeBase.width property

Gets or sets the width of the containing block of the shape.


```python
@property
def width(self) -> float:
    ...

@width.setter
def width(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# Şeklin \"RelativeHorizontalPosition\" özelliğini, \"Left\" özelliğinin değerini ele alacak şekilde yapılandırın
# sayfa sol kenarından nokta cinsinden şeklin yatay mesafesi olarak.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# Şeklin sayfa sol kenarından yatay mesafesini 100 olarak ayarlayın.
shape.left = 100
# \"RelativeVerticalPosition\" özelliğini benzer bir şekilde kullanarak şekli sayfanın üstünden 80pt aşağı konumlandırın.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# Şeklin yüksekliğini ayarlayın; bu, boyutları korumak için genişliği otomatik olarak ölçeklendirecektir.
shape.height = 125
self.assertEqual(125, shape.width)
# \"Bottom\" ve \"Right\" özellikleri, görüntünün alt ve sağ kenarlarını içerir.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

Shows how to resize a shape with an image.

```python
# "InsertImage" metodunu kullanarak bir görüntü eklediğimizde, oluşturucu görüntüyü gösteren şekli ölçeklendirir, böylece,
# Microsoft Word'de %100 yakınlaştırma ile belgeyi görüntülediğimizde, şekil görüntüyü gerçek boyutunda gösterir.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 400x400 boyutundaki bir görüntü, 300x300pt boyutunda bir ImageData nesnesi oluşturur.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Eğer bir şeklin boyutları görüntü verisinin boyutlarıyla eşleşirse,
# şekil görüntüyü orijinal boyutunda gösterir.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Şeklin genel boyutunu %50 azaltın.
# Ölçekleme faktörleri, şeklin oranlarını korumak için genişlik ve yüksekliğe aynı anda uygulanır.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# Şekli yeniden boyutlandırdığınızda, görüntü verisinin boyutu aynı kalır.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Görüntünün boyutuna dayalı bir ölçekleme uygulamak için görüntü veri boyutlarına başvurabiliriz.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

