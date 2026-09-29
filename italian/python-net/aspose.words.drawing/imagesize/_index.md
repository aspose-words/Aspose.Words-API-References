---
title: ImageSize class
linktitle: ImageSize class
articleTitle: ImageSize class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageSize class. Contains information about image size and resolution"
type: docs
weight: 210
url: /it/python-net/aspose.words.drawing/imagesize/
---

## ImageSize class

Contains information about image size and resolution.
To learn more, visit the [Working with Images](https://docs.aspose.com/words/python-net/working-with-images/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [ImageSize(width_pixels, height_pixels)](./__init__/#int_int) | Initializes width and height to the given values in pixels. Initializes resolution to 96 dpi. |
| [ImageSize(width_pixels, height_pixels, horizontal_resolution, vertical_resolution)](./__init__/#int_int_float_float) | Initializes width, height and resolution to the given values. |

### Properties

| Name | Description |
| --- | --- |
| [height_pixels](./height_pixels/) | Gets the height of the image in pixels. |
| [height_points](./height_points/) | Gets the height of the image in points. 1 point is 1/72 inch. |
| [horizontal_resolution](./horizontal_resolution/) | Gets the horizontal resolution in DPI. |
| [vertical_resolution](./vertical_resolution/) | Gets the vertical resolution in DPI. |
| [width_pixels](./width_pixels/) | Gets the width of the image in pixels. |
| [width_points](./width_points/) | Gets the width of the image in points. 1 point is 1/72 inch. |

### Examples

Shows how to resize a shape with an image.

```python
# Quando inseriamo un'immagine usando il metodo "InsertImage", il builder scala la forma che visualizza l'immagine in modo che,
# quando visualizziamo il documento con zoom al 100% in Microsoft Word, la forma visualizza l'immagine nella sua dimensione reale.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Un'immagine 400x400 creerà un oggetto ImageData con una dimensione dell'immagine di 300x300pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Se le dimensioni di una forma corrispondono alle dimensioni dei dati dell'immagine,
# allora la forma visualizza l'immagine nella sua dimensione originale.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Riduci la dimensione complessiva della forma del 50%.
# I fattori di scala si applicano sia alla larghezza che all'altezza contemporaneamente per preservare le proporzioni della forma.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# Quando ridimensioni la forma, la dimensione dei dati dell'immagine rimane invariata.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Possiamo fare riferimento alle dimensioni dei dati dell'immagine per applicare una scala basata sulla dimensione dell'immagine.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ImageData.image_size](../imagedata/image_size/)

