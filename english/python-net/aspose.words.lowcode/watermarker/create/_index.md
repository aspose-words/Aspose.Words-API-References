---
title: Watermarker.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Python
description: "Watermarker.create method. Creates new instance of the watermarker processor."
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/watermarker/create/
---

## create(context) {#watermarkercontext}

Creates new instance of the watermarker processor.


```python
def create(self, context: aspose.words.lowcode.WatermarkerContext):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| context | [WatermarkerContext](../../watermarkercontext/) |  |

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
* class [Watermarker](../)

