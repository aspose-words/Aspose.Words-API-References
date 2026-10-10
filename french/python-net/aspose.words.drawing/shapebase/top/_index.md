---
title: ShapeBase.top property
linktitle: top property
articleTitle: top property
second_title: Aspose.Words for Python
description: "ShapeBase.top property. Gets or sets the position of the top edge of the containing block of the shape."
type: docs
weight: 580
url: /fr/python-net/aspose.words.drawing/shapebase/top/
---

## ShapeBase.top property

Gets or sets the position of the top edge of the containing block of the shape.


```python
@property
def top(self) -> float:
    ...

@top.setter
def top(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.




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

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

