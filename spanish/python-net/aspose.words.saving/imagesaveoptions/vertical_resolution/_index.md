---
title: ImageSaveOptions.vertical_resolution property
linktitle: vertical_resolution property
articleTitle: vertical_resolution property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.vertical_resolution property. Gets or sets the vertical resolution for the generated images, in dots per inch."
type: docs
weight: 190
url: /es/python-net/aspose.words.saving/imagesaveoptions/vertical_resolution/
---

## ImageSaveOptions.vertical_resolution property

Gets or sets the vertical resolution for the generated images, in dots per inch.


```python
@property
def vertical_resolution(self) -> float:
    ...

@vertical_resolution.setter
def vertical_resolution(self, value: float):
    ...

```

### Remarks

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.




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

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

