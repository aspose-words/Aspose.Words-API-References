---
title: WatermarkType enumeration
linktitle: WatermarkType enumeration
articleTitle: WatermarkType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.WatermarkType enumeration. Specifies the watermark type."
type: docs
weight: 1510
url: /it/python-net/aspose.words/watermarktype/
---

## WatermarkType enumeration

Specifies the watermark type.


### Members

| Name | Description |
| --- | --- |
| TEXT | Indicates that the text will be used as a watermark. Such a watermark corresponds to a WordArt object. |
| IMAGE | Indicates that the image will be used as a watermark. Such a watermark corresponds to a shape with image. |
| NONE | Indicates watermark is no set. |

### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Aggiungi una filigrana di testo semplice.
doc.watermark.set_text(text='Aspose Watermark')
# Se desideriamo modificare la formattazione del testo usandolo come filigrana,
# possiamo farlo passando un oggetto TextWatermarkOptions durante la creazione della filigrana.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# Possiamo rimuovere una filigrana da un documento in questo modo.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../)

