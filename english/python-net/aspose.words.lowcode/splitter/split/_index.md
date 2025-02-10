---
title: Splitter.split method
linktitle: split method
articleTitle: split method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Splitter.split method"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/splitter/split/
---

## split(input_file_name, output_file_name, options) {#str_str_splitoptions}

Splits a document into multiple parts based on the specified split options and saves 
the resulting parts to files. The output file format is determined by the extension of the output file name.


```python
def split(self, input_file_name: str, output_file_name: str, options: aspose.words.lowcode.SplitOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| options | [SplitOptions](../../splitoptions/) | Document split options. |

## split(input_file_name, output_file_name, save_format, options) {#str_str_saveformat_splitoptions}

Splits a document into multiple parts based on the specified split options and saves 
the resulting parts to files in the specified save format.


```python
def split(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, options: aspose.words.lowcode.SplitOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| options | [SplitOptions](../../splitoptions/) | Document split options. |

## split(input_file_name, output_file_name, save_options, options) {#str_str_saveoptions_splitoptions}

Splits a document into multiple parts based on the specified split options and saves 
the resulting parts to files in the specified save format.


```python
def split(self, input_file_name: str, output_file_name: str, save_options: aspose.words.saving.SaveOptions, options: aspose.words.lowcode.SplitOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| options | [SplitOptions](../../splitoptions/) | Document split options. |

## split(input_stream, save_format, options) {#bytesio_saveformat_splitoptions}

Splits a document from an input stream into multiple parts based on the specified split options and 
returns the resulting parts as an array of streams in the specified save format.


```python
def split(self, input_stream: io.BytesIO, save_format: aspose.words.SaveFormat, options: aspose.words.lowcode.SplitOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| options | [SplitOptions](../../splitoptions/) | Document split options. |

## split(input_stream, save_options, options) {#bytesio_saveoptions_splitoptions}

Splits a document from an input stream into multiple parts based on the specified split options and 
returns the resulting parts as an array of streams in the specified save format.


```python
def split(self, input_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions, options: aspose.words.lowcode.SplitOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| options | [SplitOptions](../../splitoptions/) | Document split options. |

## Examples

Shows how to split document by pages.

```python
doc = MY_DIR + 'Big document.docx'
options = aw.lowcode.SplitOptions()
options.split_criteria = aw.lowcode.SplitCriteria.PAGE
aw.lowcode.Splitter.split(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.SplitDocument.1.docx', options=options)
aw.lowcode.Splitter.split(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.SplitDocument.2.docx', save_format=aw.SaveFormat.DOCX, options=options)
```

Shows how to split document from the stream by pages.

```python
with system_helper.io.FileStream(MY_DIR + 'Big document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    options = aw.lowcode.SplitOptions()
    options.split_criteria = aw.lowcode.SplitCriteria.PAGE
    stream = aw.lowcode.Splitter.split(input_stream=stream_in, save_format=aw.SaveFormat.DOCX, options=options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Splitter](../)

