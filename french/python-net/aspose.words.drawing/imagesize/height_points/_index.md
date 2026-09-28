---
title: ImageSize.height_points property
linktitle: height_points property
articleTitle: height_points property
second_title: Aspose.Words for Python
description: "ImageSize.height_points property. Gets the height of the image in points"
type: docs
weight: 30
url: /fr/python-net/aspose.words.drawing/imagesize/height_points/
---

## ImageSize.height_points property

Gets the height of the image in points. 1 point is 1/72 inch.


```python
@property
def height_points(self) -> float:
    ...

```

### Examples

Shows how to resize a shape with an image.

```python
# Lorsque nous insérons une image à l'aide de la méthode "InsertImage", le constructeur met à l'échelle la forme qui affiche l'image afin que
# lorsque nous visualisons le document avec un zoom de 100 % dans Microsoft Word, la forme affiche l'image à sa taille réelle.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Une image de 400 x 400 créera un objet ImageData avec une taille d'image de 300 x 300 pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Si les dimensions d'une forme correspondent aux dimensions des données d'image,
# alors la forme affiche l'image à sa taille d'origine.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Réduisez la taille globale de la forme de 50 %.
# Les facteurs d'échelle s'appliquent à la fois à la largeur et à la hauteur simultanément pour préserver les proportions de la forme.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# Lorsque vous redimensionnez la forme, la taille des données d'image reste la même.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Nous pouvons nous référer aux dimensions des données d'image pour appliquer une mise à l'échelle basée sur la taille de l'image.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

