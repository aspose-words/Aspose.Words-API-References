---
title: ImageSize.horizontal_resolution property
linktitle: horizontal_resolution property
articleTitle: horizontal_resolution property
second_title: Aspose.Words for Python
description: "ImageSize.horizontal_resolution property. Gets the horizontal resolution in DPI."
type: docs
weight: 40
url: /ru/python-net/aspose.words.drawing/imagesize/horizontal_resolution/
---

## ImageSize.horizontal_resolution property

Gets the horizontal resolution in DPI.


```python
@property
def horizontal_resolution(self) -> float:
    ...

```

### Examples

Shows how to read the properties of an image in a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте в документ фигуру, содержащую изображение, полученное из нашей локальной файловой системы.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Если фигура содержит изображение, её свойство ImageData будет действительным,
# и она будет содержать объект ImageSize.
image_size = shape.image_data.image_size
# Объект ImageSize содержит только для чтения информацию об изображении внутри фигуры.
self.assertEqual(400, image_size.height_pixels)
self.assertEqual(400, image_size.width_pixels)
delta = 0.05
self.assertAlmostEqual(95.98, image_size.horizontal_resolution, delta=delta)
self.assertAlmostEqual(95.98, image_size.vertical_resolution, delta=delta)
# Мы можем задавать размер фигуры, исходя из размера её изображения, чтобы избежать растягивания изображения.
shape.width = image_size.width_points * 2
shape.height = image_size.height_points * 2
doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

