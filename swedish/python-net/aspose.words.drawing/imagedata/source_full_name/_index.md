---
title: ImageData.source_full_name property
linktitle: source_full_name property
articleTitle: source_full_name property
second_title: Aspose.Words for Python
description: "ImageData.source_full_name property. Gets or sets the path and name of the source file for the linked image."
type: docs
weight: 170
url: /sv/python-net/aspose.words.drawing/imagedata/source_full_name/
---

## ImageData.source_full_name property

Gets or sets the path and name of the source file for the linked image.


```python
@property
def source_full_name(self) -> str:
    ...

@source_full_name.setter
def source_full_name(self, value: str):
    ...

```

### Remarks

The default value is an empty string.

If [ImageData.source_full_name](./) is not an empty string, the image is linked.




### Examples

Shows how to insert a linked image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
image_file_name = IMAGE_DIR + 'Windows MetaFile.wmf'
# Nedan följer två sätt att applicera en bild på en form så att den kan visa den.
# 1 -  Ställ in formen så att den innehåller bilden.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(file_name=image_file_name)
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx')
# Varje bild som vi lagrar i formen kommer att öka storleken på vårt dokument.
self.assertTrue(70000 < system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx').length())
doc.first_section.body.first_paragraph.remove_all_children()
# 2 -  Ställ in formen så att den länkar till en bildfil i det lokala filsystemet.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx')
# Att länka till bilder sparar utrymme och resulterar i ett mindre dokument.
# Dock kan dokumentet bara visa bilden korrekt medan
# bildfilen finns på den plats som formens "SourceFullName"-egenskap pekar på.
self.assertTrue(10000 > system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx').length())
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

