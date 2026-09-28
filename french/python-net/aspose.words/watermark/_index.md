---
title: Watermark class
linktitle: Watermark class
articleTitle: Watermark class
second_title: Aspose.Words for Python
description: "aspose.words.Watermark class. Represents class to work with document watermark"
type: docs
weight: 1490
url: /fr/python-net/aspose.words/watermark/
---

## Watermark class

Represents class to work with document watermark.
To learn more, visit the [Working with Watermark](https://docs.aspose.com/words/python-net/working-with-watermark/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [type](./type/) | Gets the watermark type. |

### Methods

| Name | Description |
| --- | --- |
|[ remove()](./remove/#default) | Removes the watermark. |
|[ set_image(image_path, options)](./set_image/#str_imagewatermarkoptions) |  |
|[ set_image(image_stream, options)](./set_image/#bytesio_imagewatermarkoptions) |  |
|[ set_text(text)](./set_text/#str) | Adds Text watermark into the document. |
|[ set_text(text, options)](./set_text/#str_textwatermarkoptions) | Adds Text watermark into the document. |

### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Ajoutez un filigrane en texte brut.
doc.watermark.set_text(text='Aspose Watermark')
# Si nous souhaitons modifier le formatage du texte en l'utilisant comme filigrane,
# nous pouvons le faire en passant un objet TextWatermarkOptions lors de la création du filigrane.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# Nous pouvons supprimer un filigrane d'un document de cette façon.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../)

