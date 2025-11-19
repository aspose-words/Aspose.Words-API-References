---
title: WatermarkerContext.text_watermark_options property
linktitle: text_watermark_options property
articleTitle: text_watermark_options property
second_title: Aspose.Words for Python
description: "WatermarkerContext.text_watermark_options property. Options for the image watermark."
type: docs
weight: 50
url: /python-net/aspose.words.lowcode/watermarkercontext/text_watermark_options/
---

## WatermarkerContext.text_watermark_options property

Options for the image watermark.


```python
@property
def text_watermark_options(self) -> aspose.words.TextWatermarkOptions:
    ...

```

### Examples

Shows how to insert watermark text to the document using context.

```python
doc = MY_DIR + 'Big document.docx'
watermark_text = 'This is a watermark'
watermarker_context = aw.lowcode.WatermarkerContext()
watermarker_context.text_watermark = watermark_text
watermarker_context.text_watermark_options.color = aspose.pydrawing.Color.red
aw.lowcode.Watermarker.create(watermarker_context).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.WatermarkContextText.docx').execute()
```

Shows how to insert watermark text to the document from the stream using context.

```python
watermark_text = 'This is a watermark'
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    watermarker_context = aw.lowcode.WatermarkerContext()
    watermarker_context.text_watermark = watermark_text
    watermarker_context.text_watermark_options.color = aspose.pydrawing.Color.red
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.WatermarkContextTextStream.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Watermarker.create(watermarker_context).from_stream(input=stream_in).to_stream(output=stream_out, save_format=aw.SaveFormat.DOCX).execute()
```

### See Also

* module [aspose.words.lowcode](../../)
* class [WatermarkerContext](../)

