---
title: ShapeBase.is_layout_in_cell property
linktitle: is_layout_in_cell property
articleTitle: is_layout_in_cell property
second_title: Aspose.Words for Python
description: "ShapeBase.is_layout_in_cell property. Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it."
type: docs
weight: 330
url: /fr/python-net/aspose.words.drawing/shapebase/is_layout_in_cell/
---

## ShapeBase.is_layout_in_cell property

Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it.


```python
@property
def is_layout_in_cell(self) -> bool:
    ...

@is_layout_in_cell.setter
def is_layout_in_cell(self, value: bool):
    ...

```

### Remarks

The default value is ``True``.

Has effect only for top level shapes, the property [ShapeBase.wrap_type](../wrap_type/) of which is set to value
other than [Inline](../../../aspose.words/inline/).




### Examples

Shows how to determine how to display a shape in a table cell.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.insert_cell()
builder.end_table()
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table_style.bottom_padding = 20
table_style.left_padding = 10
table_style.right_padding = 10
table_style.top_padding = 20
table_style.borders.color = drawing.Color.black
table_style.borders.line_style = aw.LineStyle.SINGLE
table.style = table_style
builder.move_to(table.first_row.first_cell.first_paragraph)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
# Définissez la propriété "IsLayoutInCell" sur "true" pour afficher la forme comme un élément en ligne à l'intérieur du paragraphe de la cellule.
# L'origine des coordonnées qui déterminera l'emplacement de la forme sera le coin supérieur gauche de la cellule de la forme.
# Si nous redimensionnons la cellule, la forme se déplacera pour maintenir la même position en partant du coin supérieur gauche de la cellule.
# Définissez la propriété "IsLayoutInCell" sur "false" pour afficher la forme comme une forme flottante indépendante.
# L'origine des coordonnées qui déterminera l'emplacement de la forme sera le coin supérieur gauche de la page,
# et la forme ne répondra à aucun redimensionnement de sa cellule.
shape.is_layout_in_cell = is_layout_in_cell
# Nous ne pouvons appliquer la propriété "IsLayoutInCell" qu'aux formes flottantes.
shape.wrap_type = aw.drawing.WrapType.NONE
doc.save(file_name=ARTIFACTS_DIR + 'Shape.LayoutInTableCell.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

