---
title: Shape.image_data property
linktitle: image_data property
articleTitle: image_data property
second_title: Aspose.Words for Python
description: "Shape.image_data property. Provides access to the image of the shape"
type: docs
weight: 120
url: /es/python-net/aspose.words.drawing/shape/image_data/
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

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

