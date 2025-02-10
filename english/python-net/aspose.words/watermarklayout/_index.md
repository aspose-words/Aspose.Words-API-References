---
title: WatermarkLayout enumeration
linktitle: WatermarkLayout enumeration
articleTitle: WatermarkLayout enumeration
second_title: Aspose.Words for Python
description: "aspose.words.WatermarkLayout enumeration. Defines layout of the watermark relative to the watermark center."
type: docs
weight: 1410
url: /python-net/aspose.words/watermarklayout/
---

## WatermarkLayout enumeration

Defines layout of the watermark relative to the watermark center.


### Members

| Name | Description |
| --- | --- |
| HORIZONTAL | Horizontal watermark layout. Corresponds to 0 degrees of rotation. |
| DIAGONAL | Diagonal watermark layout. Corresponds to 315 degrees of rotation. |

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

