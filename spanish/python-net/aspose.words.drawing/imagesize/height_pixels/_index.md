---
title: ImageSize.height_pixels property
linktitle: height_pixels property
articleTitle: height_pixels property
second_title: Aspose.Words for Python
description: "ImageSize.height_pixels property. Gets the height of the image in pixels."
type: docs
weight: 20
url: /es/python-net/aspose.words.drawing/imagesize/height_pixels/
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
# Inserte una forma en el documento que contenga una imagen tomada de nuestro sistema de archivos local.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Si la forma contiene una imagen, su propiedad ImageData será válida,
# y contendrá un objeto ImageSize.
image_size = shape.image_data.image_size
# El objeto ImageSize contiene información de solo lectura sobre la imagen dentro de la forma.
self.assertEqual(400, image_size.height_pixels)
self.assertEqual(400, image_size.width_pixels)
delta = 0.05
self.assertAlmostEqual(95.98, image_size.horizontal_resolution, delta=delta)
self.assertAlmostEqual(95.98, image_size.vertical_resolution, delta=delta)
# Podemos basar el tamaño de la forma en el tamaño de su imagen para evitar estirar la imagen.
shape.width = image_size.width_points * 2
shape.height = image_size.height_points * 2
doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

