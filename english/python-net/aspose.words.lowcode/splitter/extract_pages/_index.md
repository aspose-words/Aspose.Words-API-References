---
title: Splitter.extract_pages method
linktitle: extract_pages method
articleTitle: extract_pages method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Splitter.extract_pages method"
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/splitter/extract_pages/
---

## extract_pages(input_file_name, output_file_name, start_page_index, page_count) {#str_str_int_int}

Extracts a specified range of pages from a document file and saves the extracted pages 
to a new file. The output file format is determined by the extension of the output file name.


```python
def extract_pages(self, input_file_name: str, output_file_name: str, start_page_index: int, page_count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| start_page_index | int | The zero-based index of the first page to extract. |
| page_count | int | Number of pages to be extracted. |

## extract_pages(input_file_name, output_file_name, save_format, start_page_index, page_count) {#str_str_saveformat_int_int}

Extracts a specified range of pages from a document file and saves the extracted pages 
to a new file using the specified save format.


```python
def extract_pages(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, start_page_index: int, page_count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| start_page_index | int | The zero-based index of the first page to extract. |
| page_count | int | Number of pages to be extracted. |

## extract_pages(input_file_name, output_file_name, save_options, start_page_index, page_count) {#str_str_saveoptions_int_int}

Extracts a specified range of pages from a document file and saves the extracted pages 
to a new file using the specified save format.


```python
def extract_pages(self, input_file_name: str, output_file_name: str, save_options: aspose.words.saving.SaveOptions, start_page_index: int, page_count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| start_page_index | int | The zero-based index of the first page to extract. |
| page_count | int | Number of pages to be extracted. |

## extract_pages(input_stream, output_stream, save_format, start_page_index, page_count) {#bytesio_bytesio_saveformat_int_int}

Extracts a specified range of pages from a document stream and saves the extracted pages 
to an output stream using the specified save format.


```python
def extract_pages(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, start_page_index: int, page_count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| start_page_index | int | The zero-based index of the first page to extract. |
| page_count | int | Number of pages to be extracted. |

## extract_pages(input_stream, output_stream, save_options, start_page_index, page_count) {#bytesio_bytesio_saveoptions_int_int}

Extracts a specified range of pages from a document stream and saves the extracted pages 
to an output stream using the specified save format.


```python
def extract_pages(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions, start_page_index: int, page_count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| start_page_index | int | The zero-based index of the first page to extract. |
| page_count | int | Number of pages to be extracted. |

## Examples

Shows how to extract pages from the document.

```python
# There is a several ways to extract pages from the document:
doc = MY_DIR + 'Big document.docx'
aw.lowcode.Splitter.extract_pages(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.ExtractPages.1.docx', start_page_index=0, page_count=2)
aw.lowcode.Splitter.extract_pages(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.ExtractPages.2.docx', save_format=aw.SaveFormat.DOCX, start_page_index=0, page_count=2)
```

Shows how to extract pages from the document from the stream.

```python
with system_helper.io.FileStream(MY_DIR + 'Big document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.ExtractPagesStream.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Splitter.extract_pages(input_stream=stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, start_page_index=0, page_count=2)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Splitter](../)

