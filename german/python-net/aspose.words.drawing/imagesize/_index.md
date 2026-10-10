---
title: ImageSize class
linktitle: ImageSize class
articleTitle: ImageSize class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageSize class. Contains information about image size and resolution"
type: docs
weight: 210
url: /de/python-net/aspose.words.drawing/imagesize/
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
# Wenn wir ein Bild mit der Methode "InsertImage" einfügen, skaliert der Builder die Form, die das Bild anzeigt, sodass
# wenn wir das Dokument mit 100 % Zoom in Microsoft Word anzeigen, zeigt die Form das Bild in seiner tatsächlichen Größe an.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Ein 400 × 400‑Pixel‑Bild erzeugt ein ImageData‑Objekt mit einer Bildgröße von 300 × 300 pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Wenn die Abmessungen einer Form mit den Abmessungen der Bilddaten übereinstimmen,
# dann zeigt die Form das Bild in seiner Originalgröße an.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Reduzieren Sie die Gesamtabmessung der Form um 50 %.
# Skalierungsfaktoren gelten gleichzeitig für Breite und Höhe, um die Proportionen der Form beizubehalten.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# Wenn Sie die Form ändern, bleibt die Größe der Bilddaten unverändert.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Wir können die Abmessungen der Bilddaten heranziehen, um eine Skalierung basierend auf der Bildgröße anzuwenden.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ImageData.image_size](../imagedata/image_size/)

