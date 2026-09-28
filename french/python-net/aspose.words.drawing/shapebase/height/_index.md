---
title: ShapeBase.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "ShapeBase.height property. Gets or sets the height of the containing block of the shape."
type: docs
weight: 210
url: /fr/python-net/aspose.words.drawing/shapebase/height/
---

## ShapeBase.height property

Gets or sets the height of the containing block of the shape.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# Configurez la propriété "RelativeHorizontalPosition" de la forme pour qu'elle traite la valeur de la propriété "Left"
# comme la distance horizontale de la forme, en points, depuis le côté gauche de la page.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# Définissez la distance horizontale de la forme depuis le côté gauche de la page à 100.
shape.left = 100
# Utilisez la propriété "RelativeVerticalPosition" de manière similaire pour positionner la forme à 80 pt sous le haut de la page.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# Définissez la hauteur de la forme, ce qui ajustera automatiquement la largeur pour préserver les dimensions.
shape.height = 125
self.assertEqual(125, shape.width)
# Les propriétés "Bottom" et "Right" contiennent respectivement les bords inférieur et droit de l'image.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

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
* class [ShapeBase](../)

