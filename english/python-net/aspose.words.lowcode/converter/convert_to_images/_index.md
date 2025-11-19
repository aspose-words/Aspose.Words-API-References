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

Converts the pages of the specified input file to image files.


```python
def convert_to_images(self, input_file: str, output_file: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |

## convert_to_images(input_file, output_file, save_format) {#str_str_saveformat}

Converts the pages of the specified input file to image files in the specified format.


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

Converts the pages of the specified input file to image files using the specified save options.


```python
def convert_to_images(self, input_file: str, output_file: str, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

## convert_to_images(input_file, load_options, output_file, save_options) {#str_loadoptions_str_imagesaveoptions}

Converts the pages of the specified input file to image files using the provided load and save options.


```python
def convert_to_images(self, input_file: str, load_options: aspose.words.loading.LoadOptions, output_file: str, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) | The input document load options. |
| output_file | str | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

## convert_to_images(input_file, save_format) {#str_saveformat}

Converts the pages of the specified input file to images in the specified format and returns an array of streams containing the images.


```python
def convert_to_images(self, input_file: str, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. Only image save formats are allowed. |

### Returns

Returns array of image streams. The streams should be disposed by the end user.


## convert_to_images(input_file, save_options) {#str_imagesaveoptions}

Converts the pages of the specified input file to images using the specified save options and returns an array of streams containing the images.


```python
def convert_to_images(self, input_file: str, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

### Returns

Returns array of image streams. The streams should be disposed by the end user.


## convert_to_images(input_stream, save_format) {#bytesio_saveformat}

Converts the pages of the specified input stream to images in the specified format and returns an array of streams containing the images.


```python
def convert_to_images(self, input_stream: io.BytesIO, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. Only image save formats are allowed. |

### Returns

Returns array of image streams. The streams should be disposed by the end user.


## convert_to_images(input_stream, save_options) {#bytesio_imagesaveoptions}

Converts the pages of the specified input stream to images using the specified save options and returns an array of streams containing the images.


```python
def convert_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

### Returns

Returns array of image streams. The streams should be disposed by the end user.


## convert_to_images(input_stream, load_options, save_options) {#bytesio_loadoptions_imagesaveoptions}

Converts the pages of the specified input stream to images using the provided load and save options, and returns an array of streams containing the images.


```python
def convert_to_images(self, input_stream: io.BytesIO, load_options: aspose.words.loading.LoadOptions, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) | The input document load options. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

### Returns

Returns array of image streams. The streams should be disposed by the end user.


## convert_to_images(doc, save_format) {#document_saveformat}

Converts the pages of the specified document to images in the specified format and returns an array of streams containing the images.


```python
def convert_to_images(self, doc: aspose.words.Document, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../../aspose.words/document/) | The input document. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. Only image save formats are allowed. |

### Returns

Returns array of image streams. The streams should be disposed by the end user.


## convert_to_images(doc, save_options) {#document_imagesaveoptions}

Converts the pages of the specified document to images using the specified save options and returns an array of streams containing the images.


```python
def convert_to_images(self, doc: aspose.words.Document, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../../aspose.words/document/) | The input document. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Image save options. |

### Returns

Returns array of image streams. The streams should be disposed by the end user.


## Examples

Shows how to convert document to images.

```python
doc = MY_DIR + 'Big document.docx'
aw.lowcode.Converter.convert(input_file=doc, output_file=ARTIFACTS_DIR + 'LowCode.ConvertToImages.1.png')
aw.lowcode.Converter.convert(input_file=doc, output_file=ARTIFACTS_DIR + 'LowCode.ConvertToImages.2.jpeg', save_format=aw.SaveFormat.JPEG)
load_options = aw.loading.LoadOptions()
load_options.ignore_ole_data = False
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.page_set = aw.saving.PageSet(page=1)
aw.lowcode.Converter.convert(input_file=doc, load_options=load_options, output_file=ARTIFACTS_DIR + 'LowCode.ConvertToImages.3.png', save_options=image_save_options)
aw.lowcode.Converter.convert(input_file=doc, output_file=ARTIFACTS_DIR + 'LowCode.ConvertToImages.4.png', save_options=image_save_options)
```

Shows how to convert document to images stream.

```python
doc = MY_DIR + 'Big document.docx'
streams = aw.lowcode.Converter.convert_to_images(input_file=doc, save_format=aw.SaveFormat.PNG)
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.page_set = aw.saving.PageSet(page=1)
streams = aw.lowcode.Converter.convert_to_images(input_file=doc, save_options=image_save_options)
streams = aw.lowcode.Converter.convert_to_images(doc=aw.Document(file_name=doc), save_format=aw.SaveFormat.PNG)
streams = aw.lowcode.Converter.convert_to_images(doc=aw.Document(file_name=doc), save_options=image_save_options)
```

Shows how to convert document to images from stream.

```python
with system_helper.io.FileStream(MY_DIR + 'Big document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    streams = aw.lowcode.Converter.convert_to_images(input_stream=stream_in, save_format=aw.SaveFormat.JPEG)
    image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
    image_save_options.page_set = aw.saving.PageSet(page=1)
    streams = aw.lowcode.Converter.convert_to_images(input_stream=stream_in, save_options=image_save_options)
    load_options = aw.loading.LoadOptions()
    load_options.ignore_ole_data = False
    aw.lowcode.Converter.convert_to_images(input_stream=stream_in, load_options=load_options, save_options=image_save_options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Converter](../)

