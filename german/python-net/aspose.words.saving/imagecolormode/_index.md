---
title: ImageColorMode enumeration
linktitle: ImageColorMode enumeration
articleTitle: ImageColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageColorMode enumeration. Specifies the color mode for the generated images of document pages."
type: docs
weight: 380
url: /de/python-net/aspose.words.saving/imagecolormode/
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
# Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben, um
# ein Farbmodus für das Bild auswählen, das der Speichervorgang erzeugt.
# Wenn wir die Eigenschaft \"ImageColorMode\" auf \"ImageColorMode.BlackAndWhite\" setzen,
# wird der Speichervorgang bei der Darstellung des Dokuments eine Graustufen‑Farbreduktion anwenden.
# Wenn wir die Eigenschaft \"ImageColorMode\" auf \"ImageColorMode.Grayscale\" setzen,
# wird der Speichervorgang das Dokument in ein monochromes Bild rendern.
# Wenn wir die Eigenschaft "ImageColorMode" auf "None" setzen, wird der Speichervorgang die Standardmethode anwenden
# und bewahrt alle Farben des Dokuments im Ausgabebild.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.image_color_mode = image_color_mode
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ColorMode.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../)

