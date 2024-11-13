---
title: Converter.convert method
linktitle: convert method
articleTitle: convert method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Converter.convert method"
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/converter/convert/
---

## convert(input_file, output_file) {#str_str}

Converts the given input document into the output document using specified input output file names and its extensions.


```python
def convert(self, input_file: str, output_file: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name. |

## convert(input_file, output_file, save_format) {#str_str_saveformat}

Converts the given input document into the output document using specified input output file names and the final document format.


```python
def convert(self, input_file: str, output_file: str, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |

## convert(input_file, output_file, save_options) {#str_str_saveoptions}

Converts the given input document into the output document using specified input output file names and save options.


```python
def convert(self, input_file: str, output_file: str, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| output_file | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |

## convert(input_file, load_options, output_file, save_options) {#str_loadoptions_str_saveoptions}

Converts the given input document into the output document using specified input output file names its load/save options.


```python
def convert(self, input_file: str, load_options: aspose.words.loading.LoadOptions, output_file: str, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file | str | The input file name. |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) | The input document load options. |
| output_file | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |

## convert(input_stream, output_stream, save_format) {#bytesio_bytesio_saveformat}

Converts the given input document into a single output document using specified input and output streams.


```python
def convert(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |

## convert(input_stream, output_stream, save_options) {#bytesio_bytesio_saveoptions}

Converts the given input document into a single output document using specified input and output streams.


```python
def convert(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input streams. |
| output_stream | io.BytesIO | The output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |

## convert(input_stream, load_options, output_stream, save_options) {#bytesio_loadoptions_bytesio_saveoptions}

Converts the given input document into a single output document using specified input and output streams.


```python
def convert(self, input_stream: io.BytesIO, load_options: aspose.words.loading.LoadOptions, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input streams. |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) | The input document load options. |
| output_stream | io.BytesIO | The output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |

## Examples

Shows how to convert documents with a single line of code.

```python
aw.lowcode.Converter.convert(input_file=MY_DIR + 'Document.docx', output_file=ARTIFACTS_DIR + 'LowCode.Convert.pdf')
aw.lowcode.Converter.convert(input_file=MY_DIR + 'Document.docx', output_file=ARTIFACTS_DIR + 'LowCode.Convert.rtf', save_format=aw.SaveFormat.RTF)
save_options = aw.saving.OoxmlSaveOptions()
save_options.password = 'Aspose.Words'
aw.lowcode.Converter.convert(input_file=MY_DIR + 'Document.doc', output_file=ARTIFACTS_DIR + 'LowCode.Convert.docx', save_options=save_options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Converter](../)

