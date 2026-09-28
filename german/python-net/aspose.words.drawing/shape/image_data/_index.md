---
title: Shape.image_data property
linktitle: image_data property
articleTitle: image_data property
second_title: Aspose.Words for Python
description: "Shape.image_data property. Provides access to the image of the shape"
type: docs
weight: 120
url: /de/python-net/aspose.words.drawing/shape/image_data/
---

## Shape.image_data property

Provides access to the image of the shape.
Returns ``None`` if the shape cannot have an image.



```python
@property
def image_data(self) -> aspose.words.drawing.ImageData:
    ...

```

### Examples

Shows how to insert a linked image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
image_file_name = IMAGE_DIR + 'Windows MetaFile.wmf'
# Im Folgenden sind zwei Methoden zum Anwenden eines Bildes auf eine Form aufgeführt, damit sie es anzeigen kann.
# 1 -  Legen Sie fest, dass die Form das Bild enthält.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(file_name=image_file_name)
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx')
# Jedes Bild, das wir in einer Form speichern, erhöht die Größe unseres Dokuments.
self.assertTrue(70000 < system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx').length())
doc.first_section.body.first_paragraph.remove_all_children()
# 2 -  Legen Sie fest, dass die Form auf eine Bilddatei im lokalen Dateisystem verlinkt.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx')
# Das Verlinken von Bildern spart Speicherplatz und führt zu einem kleineren Dokument.
# Allerdings kann das Dokument das Bild nur korrekt anzeigen, solange
# Die Bilddatei befindet sich an dem Ort, auf den die Eigenschaft "SourceFullName" der Form verweist.
self.assertTrue(10000 > system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx').length())
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

