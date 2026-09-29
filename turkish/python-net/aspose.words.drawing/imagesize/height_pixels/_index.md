---
title: ImageSize.height_pixels property
linktitle: height_pixels property
articleTitle: height_pixels property
second_title: Aspose.Words for Python
description: "ImageSize.height_pixels property. Gets the height of the image in pixels."
type: docs
weight: 20
url: /tr/python-net/aspose.words.drawing/imagesize/height_pixels/
---

## ImageSize.height_pixels property

Gets the height of the image in pixels.


```python
@property
def height_pixels(self) -> int:
    ...

```

### Examples

Shows how to read the properties of an image in a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Yerel dosya sistemimizden alınan bir görüntüyü içeren bir şekli belgeye ekleyin.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Şekil bir görüntü içeriyorsa, ImageData özelliği geçerli olacaktır,
# ve bir ImageSize nesnesi içerecektir.
image_size = shape.image_data.image_size
# ImageSize nesnesi, şekil içindeki görüntüyle ilgili yalnızca okunabilir bilgileri içerir.
self.assertEqual(400, image_size.height_pixels)
self.assertEqual(400, image_size.width_pixels)
delta = 0.05
self.assertAlmostEqual(95.98, image_size.horizontal_resolution, delta=delta)
self.assertAlmostEqual(95.98, image_size.vertical_resolution, delta=delta)
# Görüntünün gerilmesini önlemek için şeklin boyutunu görüntünün boyutuna göre ayarlayabiliriz.
shape.width = image_size.width_points * 2
shape.height = image_size.height_points * 2
doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

