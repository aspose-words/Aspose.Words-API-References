---
title: ShapeBase.z_order property
linktitle: z_order property
articleTitle: z_order property
second_title: Aspose.Words for Python
description: "ShapeBase.z_order property. Determines the display order of overlapping shapes."
type: docs
weight: 650
url: /it/python-net/aspose.words.drawing/shapebase/z_order/
---

## ShapeBase.z_order property

Determines the display order of overlapping shapes.


```python
@property
def z_order(self) -> int:
    ...

@z_order.setter
def z_order(self, value: int):
    ...

```

### Remarks

Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed
as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main
text of the document.

The display order of child shapes in a group shape is determined by their order
inside the group shape.




### Examples

Shows how to manipulate the order of shapes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci tre rettangoli di colore diverso che si sovrappongono parzialmente tra loro.
# Quando inseriamo una forma che sovrappone un'altra forma, Aspose.Words posiziona la forma più recente sopra quella più vecchia.
# Il rettangolo verde chiaro sovrapporrà il rettangolo blu chiaro e lo oscurerà parzialmente,
# e il rettangolo blu chiaro oscurerà il rettangolo arancione.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=150, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=150, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.light_blue
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.light_green
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
# La proprietà "ZOrder" di una forma determina la sua priorità di impilamento rispetto alle altre forme sovrapposte.
# Se due forme sovrapposte hanno valori "ZOrder" differenti,
# Microsoft Word posizionerà la forma con valore più alto sopra la forma con valore più basso.
# Imposta i valori "ZOrder" delle nostre forme per posizionare il primo rettangolo arancione sopra il secondo rettangolo blu chiaro
# e il secondo rettangolo blu chiaro sopra il terzo rettangolo verde chiaro.
# Questo invertirà il loro ordine di impilamento originale.
shapes[0].z_order = 3
shapes[1].z_order = 2
shapes[2].z_order = 1
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ZOrder.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)
* property [ShapeBase.behind_text](../behind_text/)

