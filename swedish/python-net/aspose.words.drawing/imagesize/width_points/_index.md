---
title: ImageSize.width_points property
linktitle: width_points property
articleTitle: width_points property
second_title: Aspose.Words for Python
description: "ImageSize.width_points property. Gets the width of the image in points"
type: docs
weight: 70
url: /sv/python-net/aspose.words.drawing/imagesize/width_points/
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
# När vi infogar en bild med metoden "InsertImage" skalar byggaren formen som visar bilden så att
# när vi visar dokumentet med 100% zoom i Microsoft Word, visar formen bilden i dess faktiska storlek.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# En 400×400 bild kommer att skapa ett ImageData-objekt med en bildstorlek på 300×300pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Om en forms dimensioner matchar bilddataens dimensioner,
# så visar formen bilden i sin ursprungliga storlek.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Minska den totala storleken på formen med 50%.
# Skalningsfaktorer tillämpas på både bredd och höjd samtidigt för att bevara formens proportioner.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# När du ändrar storlek på formen förblir bilddataens storlek densamma.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Vi kan referera till bilddataens dimensioner för att tillämpa en skalning baserad på bildens storlek.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

