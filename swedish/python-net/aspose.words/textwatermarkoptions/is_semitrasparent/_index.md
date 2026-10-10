---
title: TextWatermarkOptions.is_semitrasparent property
linktitle: is_semitrasparent property
articleTitle: is_semitrasparent property
second_title: Aspose.Words for Python
description: "TextWatermarkOptions.is_semitrasparent property. Gets or sets a boolean value which is responsible for opacity of the watermark"
type: docs
weight: 50
url: /sv/python-net/aspose.words/textwatermarkoptions/is_semitrasparent/
---

## TextWatermarkOptions.is_semitrasparent property

Gets or sets a boolean value which is responsible for opacity of the watermark.
The default value is ``True``.



```python
@property
def is_semitrasparent(self) -> bool:
    ...

@is_semitrasparent.setter
def is_semitrasparent(self, value: bool):
    ...

```

### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Lägg till ett vattenmärke med vanlig text.
doc.watermark.set_text(text='Aspose Watermark')
# Om vi vill redigera textformateringen genom att använda det som ett vattenmärke,
# kan vi göra det genom att skicka ett TextWatermarkOptions-objekt när vi skapar vattenmärket.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# Vi kan ta bort ett vattenmärke från ett dokument på detta sätt.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../../)
* class [TextWatermarkOptions](../)

