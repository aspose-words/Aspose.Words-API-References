---
title: RelativeVerticalSize enumeration
linktitle: RelativeVerticalSize enumeration
articleTitle: RelativeVerticalSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeVerticalSize enumeration. Specifies relatively to what the height of a shape or a text frame is calculated vertically."
type: docs
weight: 330
url: /fr/python-net/aspose.words.drawing/relativeverticalsize/
---

## RelativeVerticalSize enumeration

Specifies relatively to what the height of a shape or a text frame is calculated vertically.


### Members

| Name | Description |
| --- | --- |
| MARGIN | Specifies that the height is calculated relatively to the space between the top and the bottom margins. |
| PAGE | Specifies that the height is calculated relatively to the page height. |
| TOP_MARGIN | Specifies that the height is calculated relatively to the top margin area size. |
| BOTTOM_MARGIN | Specifies that the height is calculated relatively to the bottom margin area size. |
| INNER_MARGIN | Specifies that the height is calculated relatively to the inside margin area size, to the top margin area size for odd pages and to the bottom margin area size for even pages. |
| OUTER_MARGIN | Specifies that the height is calculated relatively to the outside margin area size, to the bottom margin area size for odd pages and to the top margin area size for even pages. |
| DEFAULT | Default value is [RelativeVerticalSize.MARGIN](./#MARGIN). |

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

* module [aspose.words.drawing](../)
* property [ShapeBase.relative_vertical_size](../shapebase/relative_vertical_size/)

