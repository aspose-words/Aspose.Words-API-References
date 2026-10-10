---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /sv/python-net/aspose.words.drawing/shapebase/is_inline/
---

## ShapeBase.is_inline property

A quick way to determine if this shape is positioned inline with text.


```python
@property
def is_inline(self) -> bool:
    ...

```

### Remarks

Has effect only for top level shapes.




### Examples

Shows how to determine whether a shape is inline or floating.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Nedan är två omslagstyper som former kan ha.
# 1 -  Infogad:
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# En infogad form sitter inne i ett stycke bland andra stycke-element, såsom textsekvenser.
# I Microsoft Word kan vi klicka och dra formen till vilket stycke som helst som om den vore ett tecken.
# Om formen är stor kommer den att påverka vertikal styckeavstånd.
# Vi kan inte flytta den här formen till en plats utan stycke.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  Flytande:
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# En flytande form tillhör det stycke som vi infogar den i,
# vilket vi kan avgöra genom en ankarsymbol som visas när vi klickar på formen.
# Om formen inte har en synlig ankarsymbol till vänster,
# behöver vi aktivera synliga ankare via "Options" -> "Display" -> "Object Anchors".
# I Microsoft Word kan vi vänsterklicka och dra den här formen fritt till vilken plats som helst.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

