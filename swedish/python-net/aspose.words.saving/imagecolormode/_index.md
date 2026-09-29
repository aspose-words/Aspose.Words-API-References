---
title: ImageColorMode enumeration
linktitle: ImageColorMode enumeration
articleTitle: ImageColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageColorMode enumeration. Specifies the color mode for the generated images of document pages."
type: docs
weight: 380
url: /sv/python-net/aspose.words.saving/imagecolormode/
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
# När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
# välja ett färgläge för bilden som sparningsoperationen kommer att generera.
# Om vi sätter egenskapen "ImageColorMode" till "ImageColorMode.BlackAndWhite",
# kommer sparningsoperationen att tillämpa gråskala‑färgreducering medan dokumentet renderas.
# Om vi sätter egenskapen "ImageColorMode" till "ImageColorMode.Grayscale",
# kommer sparningsoperationen att rendera dokumentet till en monokrom bild.
# Om vi sätter egenskapen "ImageColorMode" till "None" kommer sparningsoperationen att använda standardmetoden
# och bevarar alla dokumentets färger i utdata‑bilden.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.image_color_mode = image_color_mode
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ColorMode.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../)

