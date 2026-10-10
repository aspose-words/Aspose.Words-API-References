---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /de/python-net/aspose.words.drawing/shapebase/is_inline/
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
# Unten sind zwei Umbruchtypen aufgeführt, die Formen haben können.
# 1 -  Inline:
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# Eine Inline-Form befindet sich innerhalb eines Absatzes zusammen mit anderen Absatzelementen, wie Textläufen.
# In Microsoft Word können wir die Form anklicken und ziehen, um sie in jeden Absatz zu verschieben, als wäre sie ein Zeichen.
# Wenn die Form groß ist, wirkt sie sich auf den vertikalen Absatzabstand aus.
# Wir können diese Form nicht an einen Ort ohne Absatz verschieben.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  Floating:
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# Eine schwebende Form gehört zu dem Absatz, in den wir sie einfügen,
# was wir anhand eines Ankersymbols erkennen können, das erscheint, wenn wir die Form anklicken.
# Wenn die Form kein sichtbares Ankersymbol zu ihrer linken Seite hat,
# müssen wir sichtbare Anker über "Options" -> "Display" -> "Object Anchors" aktivieren.
# In Microsoft Word können wir mit einem Linksklick diese Form frei an jede Position ziehen.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

