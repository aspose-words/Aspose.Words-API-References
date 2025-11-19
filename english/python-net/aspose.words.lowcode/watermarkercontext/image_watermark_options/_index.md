---
title: WatermarkerContext.image_watermark_options property
linktitle: image_watermark_options property
articleTitle: image_watermark_options property
second_title: Aspose.Words for Python
description: "WatermarkerContext.image_watermark_options property. Options for the text watermark."
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/watermarkercontext/image_watermark_options/
---

## WatermarkerContext.image_watermark_options property

Options for the text watermark.


```python
@property
def image_watermark_options(self) -> aspose.words.ImageWatermarkOptions:
    ...

```

### Examples

Shows how to insert watermark image to the document using context.

```python
doc = MY_DIR + 'Document.docx'
watermark_image = IMAGE_DIR + 'Logo.jpg'
watermarker_context = aw.lowcode.WatermarkerContext()
watermarker_context.image_watermark = system_helper.io.File.read_all_bytes(watermark_image)
watermarker_context.image_watermark_options.scale = 50
aw.lowcode.Watermarker.create(watermarker_context).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.WatermarkContextImage.docx').execute()
```

Shows how to insert watermark image to the document from a stream using context.

```python
watermark_image = IMAGE_DIR + 'Logo.jpg'
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    watermarker_context = aw.lowcode.WatermarkerContext()
    watermarker_context.image_watermark = system_helper.io.File.read_all_bytes(watermark_image)
    watermarker_context.image_watermark_options.scale = 50
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.WatermarkContextImageStream.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Watermarker.create(watermarker_context).from_stream(input=stream_in).to_stream(output=stream_out, save_format=aw.SaveFormat.DOCX).execute()
```

### See Also

* module [aspose.words.lowcode](../../)
* class [WatermarkerContext](../)

