---
title: ShapeBase.distance_left property
linktitle: distance_left property
articleTitle: distance_left property
second_title: Aspose.Words for Python
description: "ShapeBase.distance_left property. Returns or sets the distance (in points) between the document text and the left edge of the shape."
type: docs
weight: 140
url: /fr/python-net/aspose.words.drawing/shapebase/distance_left/
---

## ShapeBase.distance_left property

Returns or sets the distance (in points) between the document text and the left edge of the shape.


```python
@property
def distance_left(self) -> float:
    ...

@distance_left.setter
def distance_left(self, value: float):
    ...

```

### Remarks

The default value is 1/8 inch.

Has effect only for top level shapes.




### Examples

Shows how to set the wrapping distance for a text that surrounds a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez un rectangle et faites en sorte que le texte s'enroule étroitement autour de ses limites.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=150, height=150)
shape.wrap_type = aw.drawing.WrapType.TIGHT
# Définissez la distance minimale entre la forme et le texte environnant à 40 pt de tous les côtés.
shape.distance_top = 40
shape.distance_bottom = 40
shape.distance_left = 40
shape.distance_right = 40
# Déplacez la forme plus près du centre de la page, puis faites pivoter la forme de 60 degrés dans le sens des aiguilles d'une montre.
shape.top = 75
shape.left = 150
shape.rotation = 60
# Ajoutez du texte qui s'enroulera autour de la forme.
builder.font.size = 24
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Coordinates.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

