---
title: PageSetup.page_width property
linktitle: page_width property
articleTitle: page_width property
second_title: Aspose.Words for Python
description: "PageSetup.page_width property. Returns or sets the width of the page in points."
type: docs
weight: 340
url: /de/python-net/aspose.words/pagesetup/page_width/
---

## PageSetup.page_width property

Returns or sets the width of the page in points.


```python
@property
def page_width(self) -> float:
    ...

@page_width.setter
def page_width(self, value: float):
    ...

```

### Examples

Shows how to insert an image, and use it as a watermark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie das Bild in die Kopfzeile ein, damit es auf jeder Seite sichtbar ist.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
# Platzieren Sie das Bild in der Mitte der Seite.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.left = (builder.page_setup.page_width - shape.width) / 2
shape.top = (builder.page_setup.page_height - shape.height) / 2
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertWatermark.docx')
```

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

* module [aspose.words](../../)
* class [PageSetup](../)

