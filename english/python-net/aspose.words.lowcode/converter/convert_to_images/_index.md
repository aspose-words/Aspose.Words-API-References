---
title: Converter.convert_to_images method
linktitle: convert_to_images method
articleTitle: convert_to_images method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Converter.convert_to_images method"
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/converter/convert_to_images/
---

## convert_to_images(input_file, output_file) {#str_str}

Converts the input file pages to images.


```python
def convert_to_images(self, input_file: str, output_file: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |

## convert_to_images(input_file, output_file, save_format) {#str_str_saveformat}

Converts the input file pages to images.


```python
def convert_to_images(self, input_file: str, output_file: str, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. Only image save formats are allowed. |

## convert_to_images(input_file, output_file, save_options) {#str_str_imagesaveoptions}

Converts the input file pages to images.


```python
def convert_to_images(self, input_file: str, output_file: str, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

## convert_to_images(input_file, save_format) {#str_saveformat}

Converts the input file pages to images.


```python
def convert_to_images(self, input_file: str, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. Only image save formats are allowed. |

### Returns

Returns array of image streams. The streams should be disposed by the enduser.


## convert_to_images(input_file, save_options) {#str_imagesaveoptions}

Converts the input file pages to images.


```python
def convert_to_images(self, input_file: str, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

### Returns

Returns array of image streams. The streams should be disposed by the enduser.


## convert_to_images(input_stream, save_format) {#bytesio_saveformat}

Converts the input stream pages to images.


```python
def convert_to_images(self, input_stream: io.BytesIO, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. Only image save formats are allowed. |

### Returns

Returns array of image streams. The streams should be disposed by the enduser.


## convert_to_images(input_stream, save_options) {#bytesio_imagesaveoptions}

Converts the input stream pages to images.


```python
def convert_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

### Returns

Returns array of image streams. The streams should be disposed by the enduser.


## convert_to_images(doc, save_format) {#document_saveformat}

Converts the document pages to images.


```python
def convert_to_images(self, doc: aspose.words.Document, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../../aspose.words/document/) | The input document. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. Only image save formats are allowed. |

### Returns

Returns array of image streams. The streams should be disposed by the enduser.


## convert_to_images(doc, save_options) {#document_imagesaveoptions}

Converts the document pages to images.


```python
def convert_to_images(self, doc: aspose.words.Document, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../../aspose.words/document/) | The input document. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

### Returns

Returns array of image streams. The streams should be disposed by the enduser.


## Examples

Shows how to convert document to images.

```python
aw.lowcode.Converter.convert_to_images(input_file=MY_DIR + 'Big document.docx', output_file=ARTIFACTS_DIR + 'LowCode.ConvertToImages.png')
aw.lowcode.Converter.convert_to_images(input_file=MY_DIR + 'Big document.docx', output_file=ARTIFACTS_DIR + 'LowCode.ConvertToImages.jpeg', save_format=aw.SaveFormat.JPEG)
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.page_set = aw.saving.PageSet(page=1)
aw.lowcode.Converter.convert_to_images(input_file=MY_DIR + 'Big document.docx', output_file=ARTIFACTS_DIR + 'LowCode.ConvertToImages.png', save_options=image_save_options)
```

Shows how to convert document to images stream.

```python
streams = aw.lowcode.Converter.convert_to_images(input_file=MY_DIR + 'Big document.docx', save_format=aw.SaveFormat.PNG)
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.page_set = aw.saving.PageSet(page=1)
streams = aw.lowcode.Converter.convert_to_images(input_file=MY_DIR + 'Big document.docx', save_options=image_save_options)
streams = aw.lowcode.Converter.convert_to_images(doc=aw.Document(file_name=MY_DIR + 'Big document.docx'), save_format=aw.SaveFormat.PNG)
streams = aw.lowcode.Converter.convert_to_images(doc=aw.Document(file_name=MY_DIR + 'Big document.docx'), save_options=image_save_options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Converter](../)

