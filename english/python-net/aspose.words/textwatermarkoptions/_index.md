---
title: TextWatermarkOptions class
linktitle: TextWatermarkOptions class
articleTitle: TextWatermarkOptions class
second_title: Aspose.Words for Python
description: "aspose.words.TextWatermarkOptions class. Contains options that can be specified when adding a watermark with text"
type: docs
weight: 1300
url: /python-net/aspose.words/textwatermarkoptions/
---

## TextWatermarkOptions class

Contains options that can be specified when adding a watermark with text.
To learn more, visit the [Working with Watermark](https://docs.aspose.com/words/python-net/working-with-watermark/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [TextWatermarkOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [color](./color/) | Gets or sets font color. The default value is aspose.pydrawing.Color.silver. |
| [font_family](./font_family/) | Gets or sets font family name. The default value is "Calibri". |
| [font_size](./font_size/) | Gets or sets a font size. The default value is 0 - auto. |
| [is_semitrasparent](./is_semitrasparent/) | Gets or sets a boolean value which is responsible for opacity of the watermark. The default value is ``True``. |
| [layout](./layout/) | Gets or sets layout of the watermark. The default value is [WatermarkLayout.DIAGONAL](../watermarklayout/#DIAGONAL). |

### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Add a plain text watermark.
doc.watermark.set_text(text='Aspose Watermark')
# If we wish to edit the text formatting using it as a watermark,
# we can do so by passing a TextWatermarkOptions object when creating the watermark.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# We can remove a watermark from a document like this.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../)

