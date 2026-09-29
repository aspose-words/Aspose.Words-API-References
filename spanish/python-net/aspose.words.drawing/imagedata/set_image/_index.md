---
title: ImageData.set_image method
linktitle: set_image method
articleTitle: set_image method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageData.set_image method"
type: docs
weight: 210
url: /es/python-net/aspose.words.drawing/imagedata/set_image/
---

## set_image(stream) {#bytesio}

```python
def set_image(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO |  |

## set_image(file_name) {#str}

```python
def set_image(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

## Examples

Shows how to insert a linked image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
image_file_name = IMAGE_DIR + 'Windows MetaFile.wmf'
# A continuación se presentan dos formas de aplicar una imagen a una forma para que pueda mostrarla.
# 1 -  Configurar la forma para que contenga la imagen.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(file_name=image_file_name)
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx')
# Cada imagen que almacenemos en la forma aumentará el tamaño de nuestro documento.
self.assertTrue(70000 < system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx').length())
doc.first_section.body.first_paragraph.remove_all_children()
# 2 -  Configurar la forma para que enlace a un archivo de imagen en el sistema de archivos local.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx')
# Enlazar a imágenes ahorrará espacio y resultará en un documento más pequeño.
# Sin embargo, el documento solo puede mostrar la imagen correctamente mientras
# el archivo de imagen está presente en la ubicación a la que apunta la propiedad "SourceFullName" de la forma.
self.assertTrue(10000 > system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx').length())
```

## See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

