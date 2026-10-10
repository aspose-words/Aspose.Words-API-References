---
title: ImageData.image_size property
linktitle: image_size property
articleTitle: image_size property
second_title: Aspose.Words for Python
description: "ImageData.image_size property. Gets the information about image size and resolution."
type: docs
weight: 130
url: /de/python-net/aspose.words.drawing/imagedata/image_size/
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

* module [aspose.words.drawing](../../)
* class [ImageData](../)

