---
title: Splitter.remove_blank_pages method
linktitle: remove_blank_pages method
articleTitle: remove_blank_pages method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Splitter.remove_blank_pages method"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/splitter/remove_blank_pages/
---

## remove_blank_pages(input_file_name, output_file_name) {#str_str}

Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed.


```python
def remove_blank_pages(self, input_file_name: str, output_file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |

### Returns

List of page numbers has been considered as blank and removed.


## remove_blank_pages(input_file_name, output_file_name, save_format) {#str_str_saveformat}

Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed.


```python
def remove_blank_pages(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |

### Returns

List of page numbers has been considered as blank and removed.


## remove_blank_pages(input_file_name, output_file_name, save_options) {#str_str_saveoptions}

Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed.


```python
def remove_blank_pages(self, input_file_name: str, output_file_name: str, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |

### Returns

List of page numbers has been considered as blank and removed.


## remove_blank_pages(input_stream, output_stream, save_format) {#bytesio_bytesio_saveformat}

Removes blank pages from a document provided in an input stream and saves the updated document 
to an output stream in the specified save format. Returns a list of page numbers that were removed.


```python
def remove_blank_pages(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |

### Returns

List of page numbers has been considered as blank and removed.


## remove_blank_pages(input_stream, output_stream, save_options) {#bytesio_bytesio_saveoptions}

Removes blank pages from a document provided in an input stream and saves the updated document 
to an output stream in the specified save format. Returns a list of page numbers that were removed.


```python
def remove_blank_pages(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |

### Returns

List of page numbers has been considered as blank and removed.


## Examples

Shows how to remove empty pages from the document.

```python
# There is a several ways to remove empty pages from the document:
doc = MY_DIR + 'Blank pages.docx'
aw.lowcode.Splitter.remove_blank_pages(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.RemoveBlankPages.1.docx')
aw.lowcode.Splitter.remove_blank_pages(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.RemoveBlankPages.2.docx', save_format=aw.SaveFormat.DOCX)
```

Shows how to remove empty pages from the document from the stream.

```python
with system_helper.io.FileStream(MY_DIR + 'Blank pages.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.RemoveBlankPagesStream.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Splitter.remove_blank_pages(input_stream=stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Splitter](../)

