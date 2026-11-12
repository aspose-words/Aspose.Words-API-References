---
title: ImageData.image_size property
linktitle: image_size property
articleTitle: image_size property
second_title: Aspose.Words for Python
description: "ImageData.image_size property. Gets the information about image size and resolution."
type: docs
weight: 130
url: /tr/python-net/aspose.words.drawing/imagedata/image_size/
---

## ImageData.image_size property

Gets the information about image size and resolution.


```python
@property
def image_size(self) -> aspose.words.drawing.ImageSize:
    ...

```

### Remarks

If the image is linked only and not stored in the document, returns zero size.




### Examples

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
* class [ImageData](../)

