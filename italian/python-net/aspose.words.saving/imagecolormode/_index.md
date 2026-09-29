---
title: ImageColorMode enumeration
linktitle: ImageColorMode enumeration
articleTitle: ImageColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageColorMode enumeration. Specifies the color mode for the generated images of document pages."
type: docs
weight: 380
url: /it/python-net/aspose.words.saving/imagecolormode/
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
# Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
# seleziona una modalità colore per l'immagine che l'operazione di salvataggio genererà.
# Se impostiamo la proprietà "ImageColorMode" su "ImageColorMode.BlackAndWhite",
# l'operazione di salvataggio applicherà una riduzione del colore in scala di grigi durante il rendering del documento.
# Se impostiamo la proprietà "ImageColorMode" su "ImageColorMode.Grayscale",
# l'operazione di salvataggio renderà il documento in un'immagine monocromatica.
# Se impostiamo la proprietà "ImageColorMode" su "None", l'operazione di salvataggio applicherà il metodo predefinito
# e preserva tutti i colori del documento nell'immagine di output.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.image_color_mode = image_color_mode
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ColorMode.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../)

