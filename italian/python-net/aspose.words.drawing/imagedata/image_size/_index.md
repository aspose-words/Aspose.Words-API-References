---
title: ImageData.image_size property
linktitle: image_size property
articleTitle: image_size property
second_title: Aspose.Words for Python
description: "ImageData.image_size property. Gets the information about image size and resolution."
type: docs
weight: 130
url: /it/python-net/aspose.words.drawing/imagedata/image_size/
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

* module [aspose.words.drawing](../../)
* class [ImageData](../)

