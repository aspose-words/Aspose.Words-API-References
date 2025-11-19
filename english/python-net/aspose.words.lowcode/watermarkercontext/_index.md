---
title: WatermarkerContext class
linktitle: WatermarkerContext class
articleTitle: WatermarkerContext class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.WatermarkerContext class. Document watermarker context."
type: docs
weight: 250
url: /python-net/aspose.words.lowcode/watermarkercontext/
---

## WatermarkerContext class

Document watermarker context.


**Inheritance:** [WatermarkerContext](./) → [ProcessorContext](../processorcontext/)

### Constructors
| Name | Description |
| --- | --- |
| [WatermarkerContext()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [font_settings](../processorcontext/font_settings/) | Font settings used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [image_watermark](./image_watermark/) | Image bytes to be used as a watermark. |
| [image_watermark_options](./image_watermark_options/) | Options for the text watermark. |
| [layout_options](../processorcontext/layout_options/) | Document layout options used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [text_watermark](./text_watermark/) | Text to be used as a watermark. |
| [text_watermark_options](./text_watermark_options/) | Options for the image watermark. |
| [warning_callback](../processorcontext/warning_callback/) | Warning callback used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |

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

* module [aspose.words.lowcode](../)
* class [ProcessorContext](../processorcontext/)

