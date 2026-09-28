---
title: TextWatermarkOptions.layout property
linktitle: layout property
articleTitle: layout property
second_title: Aspose.Words for Python
description: "TextWatermarkOptions.layout property. Gets or sets layout of the watermark"
type: docs
weight: 60
url: /de/python-net/aspose.words/textwatermarkoptions/layout/
---

## TextWatermarkOptions.layout property

Gets or sets layout of the watermark. The default value is [WatermarkLayout.DIAGONAL](../../watermarklayout/#DIAGONAL).



```python
@property
def layout(self) -> aspose.words.WatermarkLayout:
    ...

@layout.setter
def layout(self, value: aspose.words.WatermarkLayout):
    ...

```

### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Fügen Sie ein Wasserzeichen aus einfachem Text hinzu.
doc.watermark.set_text(text='Aspose Watermark')
# Wenn wir die Textformatierung bearbeiten möchten, indem wir es als Wasserzeichen verwenden,
# können wir dies tun, indem wir beim Erstellen des Wasserzeichens ein TextWatermarkOptions-Objekt übergeben.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# Wir können ein Wasserzeichen aus einem Dokument wie folgt entfernen.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../../)
* class [TextWatermarkOptions](../)

