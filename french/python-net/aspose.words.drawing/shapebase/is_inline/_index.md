---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /fr/python-net/aspose.words.drawing/shapebase/is_inline/
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
# Ci-dessous, deux types d'enveloppage que les formes peuvent avoir.
# 1 -  En ligne :
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# Une forme en ligne se trouve à l'intérieur d'un paragraphe parmi d'autres éléments de paragraphe, tels que des fragments de texte.
# Dans Microsoft Word, nous pouvons cliquer et faire glisser la forme vers n'importe quel paragraphe comme si c'était un caractère.
# Si la forme est grande, elle affectera l'espacement vertical du paragraphe.
# Nous ne pouvons pas déplacer cette forme vers un endroit sans paragraphe.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  Flottante :
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# Une forme flottante appartient au paragraphe dans lequel nous l'insérons,
# ce que nous pouvons déterminer grâce à un symbole d'ancre qui apparaît lorsque nous cliquons sur la forme.
# Si la forme n'a pas de symbole d'ancre visible à sa gauche,
# nous devrons activer les ancres visibles via "Options" -> "Display" -> "Object Anchors".
# Dans Microsoft Word, nous pouvons cliquer gauche et faire glisser cette forme librement vers n'importe quel emplacement.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

