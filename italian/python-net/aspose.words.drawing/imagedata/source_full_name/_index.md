---
title: ImageData.source_full_name property
linktitle: source_full_name property
articleTitle: source_full_name property
second_title: Aspose.Words for Python
description: "ImageData.source_full_name property. Gets or sets the path and name of the source file for the linked image."
type: docs
weight: 170
url: /it/python-net/aspose.words.drawing/imagedata/source_full_name/
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
# Di seguito sono riportati due modi per applicare un'immagine a una forma in modo che possa visualizzarla.
# 1 -  Imposta la forma per contenere l'immagine.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(file_name=image_file_name)
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx')
# Ogni immagine che memorizziamo nella forma aumenterà la dimensione del nostro documento.
self.assertTrue(70000 < system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx').length())
doc.first_section.body.first_paragraph.remove_all_children()
# 2 -  Imposta la forma per collegarsi a un file immagine nel file system locale.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx')
# Collegare le immagini farà risparmiare spazio e porterà a un documento più piccolo.
# Tuttavia, il documento può visualizzare correttamente l'immagine solo mentre
# Il file immagine è presente nella posizione a cui punta la proprietà "SourceFullName" della forma.
self.assertTrue(10000 > system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx').length())
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

