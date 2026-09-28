---
title: ShapeBase.right property
linktitle: right property
articleTitle: right property
second_title: Aspose.Words for Python
description: "ShapeBase.right property. Gets the position of the right edge of the containing block of the shape."
type: docs
weight: 490
url: /de/python-net/aspose.words.drawing/shapebase/right/
---

## ShapeBase.right property

Gets the position of the right edge of the containing block of the shape.


```python
@property
def right(self) -> float:
    ...

```

### Remarks

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# Konfigurieren Sie die Eigenschaft "RelativeHorizontalPosition" der Form, damit der Wert der Eigenschaft "Left" behandelt wird
# als horizontaler Abstand der Form, in Punkten, von der linken Seite der Seite.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# Setzen Sie den horizontalen Abstand der Form von der linken Seite der Seite auf 100.
shape.left = 100
# Verwenden Sie die Eigenschaft "RelativeVerticalPosition" auf ähnliche Weise, um die Form 80pt unterhalb des oberen Randes der Seite zu positionieren.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# Setzen Sie die Höhe der Form, wodurch die Breite automatisch skaliert wird, um die Abmessungen beizubehalten.
shape.height = 125
self.assertEqual(125, shape.width)
# Die Eigenschaften "Bottom" und "Right" enthalten die unteren bzw. rechten Kanten des Bildes.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

