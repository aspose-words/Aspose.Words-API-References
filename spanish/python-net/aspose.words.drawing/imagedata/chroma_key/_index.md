---
title: ImageData.chroma_key property
linktitle: chroma_key property
articleTitle: chroma_key property
second_title: Aspose.Words for Python
description: "ImageData.chroma_key property. Defines the color value of the image that will be treated as transparent."
type: docs
weight: 40
url: /es/python-net/aspose.words.drawing/imagedata/chroma_key/
---

## ImageData.chroma_key property

Defines the color value of the image that will be treated as transparent.


```python
@property
def chroma_key(self) -> aspose.pydrawing.Color:
    ...

@chroma_key.setter
def chroma_key(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

The default value is 0.




### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
dst_doc = aw.Document()
# Importe una forma del documento fuente y añádala al primer párrafo.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# La forma importada contiene una imagen. Podemos acceder a las propiedades y datos sin procesar de la imagen mediante el objeto ImageData.
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# Si una imagen no tiene bordes, su objeto ImageData definirá el color del borde como vacío.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# Esta imagen no enlaza a otra forma o archivo de imagen en el sistema de archivos local.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# Las propiedades "Brightness" y "Contrast" definen el brillo y el contraste de la imagen
# en una escala de 0-1, con el valor predeterminado en 0.5.
image_data.brightness = 0.8
image_data.contrast = 1
# Los valores de brillo y contraste anteriores han creado una imagen con mucho blanco.
# Podemos seleccionar un color con la propiedad ChromaKey para reemplazarlo con transparencia, como el blanco.
image_data.chroma_key = aspose.pydrawing.Color.white
# Importa la forma fuente nuevamente y establece la imagen a monocromo.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# Importa la forma fuente nuevamente para crear una tercera imagen y establécela a BiLevel.
# BiLevel establece cada píxel en negro o blanco, lo que esté más cerca del color original.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# El recorte se determina en una escala de 0-1. Recortar un lado en 0.3
# recortará el 30 % de la imagen en el lado recortado.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

