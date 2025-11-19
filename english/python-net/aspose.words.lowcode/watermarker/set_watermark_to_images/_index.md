---
title: Watermarker.set_watermark_to_images method
linktitle: set_watermark_to_images method
articleTitle: set_watermark_to_images method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Watermarker.set_watermark_to_images method"
type: docs
weight: 40
url: /python-net/aspose.words.lowcode/watermarker/set_watermark_to_images/
---

## set_watermark_to_images(input_file_name, save_options, watermark_text) {#str_imagesaveoptions_str}

Adds a text watermark into the document with options. Renders the output to images.


```python
def set_watermark_to_images(self, input_file_name: str, save_options: aspose.words.saving.ImageSaveOptions, watermark_text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| watermark_text | str | Text that is displayed as a watermark. |

## set_watermark_to_images(input_file_name, save_options, watermark_text, options) {#str_imagesaveoptions_str_textwatermarkoptions}

Adds a text watermark into the document with options. Renders the output to images.


```python
def set_watermark_to_images(self, input_file_name: str, save_options: aspose.words.saving.ImageSaveOptions, watermark_text: str, options: aspose.words.TextWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| watermark_text | str | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

## set_watermark_to_images(input_stream, save_options, watermark_text) {#bytesio_imagesaveoptions_str}

Adds a text watermark into the document with options. Renders the output to images.


```python
def set_watermark_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions, watermark_text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| watermark_text | str | Text that is displayed as a watermark. |

## set_watermark_to_images(input_stream, save_options, watermark_text, options) {#bytesio_imagesaveoptions_str_textwatermarkoptions}

Adds a text watermark into the document with options. Renders the output to images.


```python
def set_watermark_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions, watermark_text: str, options: aspose.words.TextWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| watermark_text | str | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

## set_watermark_to_images(input_file_name, save_options, watermark_image_bytes) {#str_imagesaveoptions_bytes}

Adds an image watermark into the document with options. Renders the output to images.


```python
def set_watermark_to_images(self, input_file_name: str, save_options: aspose.words.saving.ImageSaveOptions, watermark_image_bytes: bytes):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| watermark_image_bytes | bytes | Image bytes that is displayed as a watermark. |

## set_watermark_to_images(input_file_name, save_options, watermark_image_bytes, options) {#str_imagesaveoptions_bytes_imagewatermarkoptions}

Adds an image watermark into the document with options. Renders the output to images.


```python
def set_watermark_to_images(self, input_file_name: str, save_options: aspose.words.saving.ImageSaveOptions, watermark_image_bytes: bytes, options: aspose.words.ImageWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| watermark_image_bytes | bytes | Image bytes that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

## set_watermark_to_images(input_stream, save_options, watermark_image_stream) {#bytesio_imagesaveoptions_bytesio}

Adds an image watermark into the document with options. Renders the output to images.


```python
def set_watermark_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions, watermark_image_stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| watermark_image_stream | io.BytesIO | Image stream that is displayed as a watermark. |

## set_watermark_to_images(input_stream, save_options, watermark_image_stream, options) {#bytesio_imagesaveoptions_bytesio_imagewatermarkoptions}

Adds an image watermark into the document with options. Renders the output to images.


```python
def set_watermark_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions, watermark_image_stream: io.BytesIO, options: aspose.words.ImageWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| watermark_image_stream | io.BytesIO | Image stream that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

## Examples

Shows how to insert watermark text to the document and save result to images.

```python
doc = MY_DIR + 'Big document.docx'
watermark_text = 'This is a watermark'
images = aw.lowcode.Watermarker.set_watermark_to_images(input_file_name=doc, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), watermark_text=watermark_text)
watermark_options = aw.TextWatermarkOptions()
watermark_options.color = aspose.pydrawing.Color.red
images = aw.lowcode.Watermarker.set_watermark_to_images(input_file_name=doc, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), watermark_text=watermark_text, options=watermark_options)
```

Shows how to insert watermark text to the document from the stream and save result to images.

```python
watermark_text = 'This is a watermark'
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    images = aw.lowcode.Watermarker.set_watermark_to_images(input_stream=stream_in, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), watermark_text=watermark_text)
    watermark_options = aw.TextWatermarkOptions()
    watermark_options.color = aspose.pydrawing.Color.red
    images = aw.lowcode.Watermarker.set_watermark_to_images(input_stream=stream_in, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), watermark_text=watermark_text, options=watermark_options)
```

Shows how to insert watermark image to the document and save result to images.

```python
doc = MY_DIR + 'Document.docx'
watermark_image = IMAGE_DIR + 'Logo.jpg'
aw.lowcode.Watermarker.set_watermark_to_images(input_file_name=doc, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), watermark_image_bytes=system_helper.io.File.read_all_bytes(watermark_image))
options = aw.ImageWatermarkOptions()
options.scale = 50
aw.lowcode.Watermarker.set_watermark_to_images(input_file_name=doc, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), watermark_image_bytes=system_helper.io.File.read_all_bytes(watermark_image), options=options)
```

Shows how to insert watermark image to the document from a stream and save result to images.

```python
watermark_image = IMAGE_DIR + 'Logo.jpg'
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    with system_helper.io.FileStream(watermark_image, system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as image_stream:
        aw.lowcode.Watermarker.set_watermark_to_images(input_stream=stream_in, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), watermark_image_stream=image_stream)
        options = aw.ImageWatermarkOptions()
        options.scale = 50
        aw.lowcode.Watermarker.set_watermark_to_images(input_stream=stream_in, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), watermark_image_stream=image_stream, options=options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Watermarker](../)

