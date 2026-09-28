---
title: ShapeBase.relative_horizontal_size property
linktitle: relative_horizontal_size property
articleTitle: relative_horizontal_size property
second_title: Aspose.Words for Python
description: "ShapeBase.relative_horizontal_size property. Gets or sets the value of shape's relative size in horizontal direction."
type: docs
weight: 460
url: /fr/python-net/aspose.words.drawing/shapebase/relative_horizontal_size/
---

## ShapeBase.relative_horizontal_size property

Gets or sets the value of shape's relative size in horizontal direction.


```python
@property
def relative_horizontal_size(self) -> aspose.words.drawing.RelativeHorizontalSize:
    ...

@relative_horizontal_size.setter
def relative_horizontal_size(self, value: aspose.words.drawing.RelativeHorizontalSize):
    ...

```

### Remarks

The default value is [RelativeHorizontalSize](../../relativehorizontalsize/).

Has effect only if [ShapeBase.width_relative](../width_relative/) is set.




### Examples

Shows how to set relative size and position.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ajout d'une forme simple avec une taille et une position absolues.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=40)
# Définissez WrapType sur WrapType.None car les formes en ligne sont automatiquement converties en unités absolues.
shape.wrap_type = aw.drawing.WrapType.NONE
# Vérification et définition de la taille horizontale relative.
if shape.relative_horizontal_size == aw.drawing.RelativeHorizontalSize.DEFAULT:
    # Définir la liaison de la taille horizontale sur Margin.
    shape.relative_horizontal_size = aw.drawing.RelativeHorizontalSize.MARGIN
    # Définir la largeur à 50 % de la largeur de Margin.
    shape.width_relative = 50
# Vérification et définition de la taille verticale relative.
if shape.relative_vertical_size == aw.drawing.RelativeVerticalSize.DEFAULT:
    # Définir la liaison de la taille verticale sur Margin.
    shape.relative_vertical_size = aw.drawing.RelativeVerticalSize.MARGIN
    # Définir la hauteur à 30 % de la hauteur de Margin.
    shape.height_relative = 30
# Vérification et définition de la position verticale relative.
if shape.relative_vertical_position == aw.drawing.RelativeVerticalPosition.PARAGRAPH:
    # Définir la liaison de la position sur TopMargin.
    shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.TOP_MARGIN
    # Définir le haut relatif à 30 % de la position TopMargin.
    shape.top_relative = 30
# Vérification et définition de la position horizontale relative.
if shape.relative_horizontal_position == aw.drawing.RelativeHorizontalPosition.DEFAULT:
    # Définir la liaison de la position sur RightMargin.
    shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN
    # La valeur relative de la position peut être négative.
    shape.left_relative = -260
doc.save(file_name=ARTIFACTS_DIR + 'Shape.RelativeSizeAndPosition.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

