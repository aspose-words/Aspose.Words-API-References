---
title: TextWatermarkOptions.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "TextWatermarkOptions.color property. Gets or sets font color"
type: docs
weight: 20
url: /it/python-net/aspose.words/textwatermarkoptions/color/
---

## TextWatermarkOptions.color property

Gets or sets font color. The default value is aspose.pydrawing.Color.silver.



```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

@color.setter
def color(self, value: aspose.pydrawing.Color):
    ...

```

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

* module [aspose.words](../../)
* class [TextWatermarkOptions](../)

