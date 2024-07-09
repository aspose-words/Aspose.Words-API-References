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

Convert the input file pages to images.


```python
def convert_to_images(self, input_file: str, output_file: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |

## convert_to_images(input_file, output_file, save_format) {#str_str_saveformat}

Convert the input file pages to images.


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

Convert the input file pages to images.


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

Convert the input file pages to images.


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

Convert the input file pages to images.


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

Convert the input stream pages to images.


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

Convert the input stream pages to images.


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

Convert the document pages to images.


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

Convert the document pages to images.


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


## See Also

* module [aspose.words.lowcode](../../)
* class [Converter](../)

