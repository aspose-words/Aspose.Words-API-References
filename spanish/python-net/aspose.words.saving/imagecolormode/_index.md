---
title: ImageColorMode enumeration
linktitle: ImageColorMode enumeration
articleTitle: ImageColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageColorMode enumeration. Specifies the color mode for the generated images of document pages."
type: docs
weight: 380
url: /es/python-net/aspose.words.saving/imagecolormode/
---

## ImageColorMode enumeration

Specifies the color mode for the generated images of document pages.


### Members

| Name | Description |
| --- | --- |
| NONE | The pages of the document will be rendered as color images. |
| GRAYSCALE | The pages of the document will be rendered as grayscale images. |
| BLACK_AND_WHITE | The pages of the document will be rendered as black and white images. |

### Examples

Shows how to set a color mode when rendering documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Al guardar el documento como imagen, podemos pasar un objeto SaveOptions a
# seleccionar un modo de color para la imagen que generará la operación de guardado.
# Si establecemos la propiedad "ImageColorMode" a "ImageColorMode.BlackAndWhite",
# la operación de guardado aplicará una reducción de color en escala de grises al renderizar el documento.
# Si establecemos la propiedad "ImageColorMode" a "ImageColorMode.Grayscale",
# la operación de guardado renderizará el documento en una imagen monocroma.
# Si establecemos la propiedad "ImageColorMode" a "None", la operación de guardado aplicará el método predeterminado
# y preservará todos los colores del documento en la imagen de salida.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.image_color_mode = image_color_mode
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ColorMode.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../)

