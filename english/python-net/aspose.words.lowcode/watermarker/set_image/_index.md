---
title: Watermarker.set_image method
linktitle: set_image method
articleTitle: set_image method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Watermarker.set_image method"
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/watermarker/set_image/
---

## set_image(input_file_name, output_file_name, watermark_image_file_name) {#str_str_str}

Adds Image watermark into the document.


```python
def set_image(self, input_file_name: str, output_file_name: str, watermark_image_file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| watermark_image_file_name | str | Image that is displayed as a watermark. |

## set_image(input_file_name, output_file_name, save_format, watermark_image_file_name) {#str_str_saveformat_str}

Adds Image watermark into the document.


```python
def set_image(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, watermark_image_file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| watermark_image_file_name | str | Image that is displayed as a watermark. |

## set_image(input_file_name, output_file_name, watermark_image_file_name, options) {#str_str_str_imagewatermarkoptions}

Adds Image watermark into the document.


```python
def set_image(self, input_file_name: str, output_file_name: str, watermark_image_file_name: str, options: aspose.words.ImageWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| watermark_image_file_name | str | Image that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

## set_image(input_file_name, output_file_name, save_format, watermark_image_file_name, options) {#str_str_saveformat_str_imagewatermarkoptions}

Adds Image watermark into the document.


```python
def set_image(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, watermark_image_file_name: str, options: aspose.words.ImageWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| watermark_image_file_name | str | Image that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/) | Defines additional options for the image watermark. |

## Examples

Shows how to insert watermark image to the document.

```python
doc = MY_DIR + 'Document.docx'
watermark_image = IMAGE_DIR + 'Logo.jpg'
aw.lowcode.Watermarker.set_image(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.SetWatermarkImage.1.docx', watermark_image_file_name=watermark_image)
aw.lowcode.Watermarker.set_image(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.SetWatermarkText.2.docx', save_format=aw.SaveFormat.DOCX, watermark_image_file_name=watermark_image)
options = aw.ImageWatermarkOptions()
options.scale = 50
aw.lowcode.Watermarker.set_image(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.SetWatermarkText.3.docx', watermark_image_file_name=watermark_image, options=options)
aw.lowcode.Watermarker.set_image(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.SetWatermarkText.4.docx', save_format=aw.SaveFormat.DOCX, watermark_image_file_name=watermark_image, options=options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Watermarker](../)

