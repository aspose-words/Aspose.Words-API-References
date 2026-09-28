---
title: ShapeBase.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "ShapeBase.height property. Gets or sets the height of the containing block of the shape."
type: docs
weight: 210
url: /de/python-net/aspose.words.drawing/shapebase/height/
---

## ShapeBase.height property

Gets or sets the height of the containing block of the shape.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




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

Shows how to resize a shape with an image.

```python
# Wenn wir ein Bild mit der Methode "InsertImage" einfügen, skaliert der Builder die Form, die das Bild anzeigt, sodass
# wenn wir das Dokument mit 100 % Zoom in Microsoft Word anzeigen, zeigt die Form das Bild in seiner tatsächlichen Größe an.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Ein 400 × 400‑Pixel‑Bild erzeugt ein ImageData‑Objekt mit einer Bildgröße von 300 × 300 pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Wenn die Abmessungen einer Form mit den Abmessungen der Bilddaten übereinstimmen,
# dann zeigt die Form das Bild in seiner Originalgröße an.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Reduzieren Sie die Gesamtabmessung der Form um 50 %.
# Skalierungsfaktoren gelten gleichzeitig für Breite und Höhe, um die Proportionen der Form beizubehalten.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# Wenn Sie die Form ändern, bleibt die Größe der Bilddaten unverändert.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Wir können die Abmessungen der Bilddaten heranziehen, um eine Skalierung basierend auf der Bildgröße anzuwenden.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

