---
title: ImageSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.save_format property. Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used"
type: docs
weight: 130
url: /es/python-net/aspose.words.saving/imagesaveoptions/save_format/
---

## ImageSaveOptions.save_format property

Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used.
Can be a raster
[SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP),
[SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG) or vector [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS),
[SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P), [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Remarks

The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [ImageSaveOptions](../) and via [SvgSaveOptions](../../svgsaveoptions/).




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

