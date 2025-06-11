---
title: Watermark.set_image method
linktitle: set_image method
articleTitle: set_image method
second_title: Aspose.Words for Python
description: "aspose.words.Watermark.set_image method"
type: docs
weight: 30
url: /python-net/aspose.words/watermark/set_image/
---

## set_image(image_path, options) {#str_imagewatermarkoptions}

```python
def set_image(self, image_path: str, options: aspose.words.ImageWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_path | str |  |
| options | [ImageWatermarkOptions](../../imagewatermarkoptions/) |  |

## set_image(image_stream, options) {#bytesio_imagewatermarkoptions}

```python
def set_image(self, image_stream: io.BytesIO, options: aspose.words.ImageWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_stream | io.BytesIO |  |
| options | [ImageWatermarkOptions](../../imagewatermarkoptions/) |  |

## Examples

Shows how to create a watermark from an image stream.

```python
doc = aw.Document()
# Modify the image watermark's appearance with an ImageWatermarkOptions object,
# then pass it while creating a watermark from an image file.
image_watermark_options = aw.ImageWatermarkOptions()
image_watermark_options.scale = 5
with system_helper.io.FileStream(IMAGE_DIR + 'Logo.jpg', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as image_stream:
    doc.watermark.set_image(image_stream=image_stream, options=image_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.ImageWatermarkStream.docx')
```

## See Also

* module [aspose.words](../../)
* class [Watermark](../)

