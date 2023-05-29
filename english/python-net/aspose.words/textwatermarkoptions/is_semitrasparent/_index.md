---
title: TextWatermarkOptions.is_semitrasparent property
linktitle: is_semitrasparent property
articleTitle: is_semitrasparent property
second_title: Aspose.Words for Python
description: "TextWatermarkOptions.is_semitrasparent property. Gets or sets a boolean value which is responsible for opacity of the watermark"
type: docs
weight: 50
url: /python-net/aspose.words/textwatermarkoptions/is_semitrasparent/
---

## TextWatermarkOptions.is_semitrasparent property

Gets or sets a boolean value which is responsible for opacity of the watermark.
The default value is ``True``.



### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()

# Add a plain text watermark.
doc.watermark.set_text("Aspose Watermark")

# If we wish to edit the text formatting using it as a watermark,
# we can do so by passing a TextWatermarkOptions object when creating the watermark.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = "Arial"
text_watermark_options.font_size = 36
text_watermark_options.color = drawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False

doc.watermark.set_text("Aspose Watermark", text_watermark_options)

doc.save(ARTIFACTS_DIR + "Document.text_watermark.docx")

# We can remove a watermark from a document like this.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../../)
* class [TextWatermarkOptions](../)

