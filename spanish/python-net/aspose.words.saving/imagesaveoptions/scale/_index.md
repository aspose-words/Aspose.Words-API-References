---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /es/python-net/aspose.words.saving/imagesaveoptions/scale/
---

## ImageSaveOptions.scale property

Gets or sets the zoom factor for the generated images.


```python
@property
def scale(self) -> float:
    ...

@scale.setter
def scale(self, value: float):
    ...

```

### Remarks

The default value is 1.0. The value must be greater than 0.


### Examples

Shows how to edit the image while Aspose.Words converts a document to one.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Al guardar el documento como imagen, podemos pasar un objeto SaveOptions a
# edite la imagen mientras la operación de guardado la renderiza.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Podemos ajustar estas propiedades para cambiar el brillo y el contraste de la imagen.
# Ambas están en una escala de 0 a 1 y su valor predeterminado es 0.5.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Podemos ajustar la resolución horizontal y vertical con estas propiedades.
# Esto afectará las dimensiones de la imagen.
# El valor predeterminado para estas propiedades es 96.0, para una resolución de 96 dpi.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Podemos escalar la imagen usando esta propiedad. El valor predeterminado es 1.0, para un escalado del 100%.
# Podemos usar esta propiedad para anular cualquier cambio en las dimensiones de la imagen que causaría cambiar la resolución.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# Crea un objeto "ImageSaveOptions" para pasar al método "Save" del renderizador de nodos y modificar
# cómo renderiza el nodo OfficeMath en una imagen.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Establece la propiedad "Scale" a 5 para renderizar el objeto a cinco veces su tamaño original.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

