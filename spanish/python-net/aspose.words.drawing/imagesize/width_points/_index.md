---
title: ImageSize.width_points property
linktitle: width_points property
articleTitle: width_points property
second_title: Aspose.Words for Python
description: "ImageSize.width_points property. Gets the width of the image in points"
type: docs
weight: 70
url: /es/python-net/aspose.words.drawing/imagesize/width_points/
---

## ImageSize.width_points property

Gets the width of the image in points. 1 point is 1/72 inch.


```python
@property
def width_points(self) -> float:
    ...

```

### Examples

Shows how to resize a shape with an image.

```python
# Cuando insertamos una imagen usando el método "InsertImage", el generador escala la forma que muestra la imagen de modo que,
# cuando vemos el documento con un zoom del 100 % en Microsoft Word, la forma muestra la imagen en su tamaño real.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Una imagen de 400 x 400 creará un objeto ImageData con un tamaño de imagen de 300 x 300 pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Si las dimensiones de una forma coinciden con las dimensiones de los datos de la imagen,
# entonces la forma muestra la imagen en su tamaño original.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Reduzca el tamaño total de la forma en un 50 %.
# Los factores de escala se aplican tanto al ancho como a la altura simultáneamente para preservar las proporciones de la forma.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# Al redimensionar la forma, el tamaño de los datos de la imagen permanece igual.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Podemos referirnos a las dimensiones de los datos de la imagen para aplicar una escala basada en el tamaño de la imagen.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

