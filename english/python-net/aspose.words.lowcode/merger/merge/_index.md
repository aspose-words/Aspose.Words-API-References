---
title: Merger.merge method
linktitle: merge method
articleTitle: merge method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Merger.merge method"
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/merger/merge/
---

## merge(output_file, input_files) {#str_strlist}

Merges the given input documents into a single output document using specified input and output file names.


```python
def merge(self, output_file: str, input_files: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_file | str |  |
| input_files | List[str] |  |

By default [MergeFormatMode.KEEP_SOURCE_FORMATTING](../../mergeformatmode/#KEEP_SOURCE_FORMATTING) is used.




## merge(output_file, input_files, save_format, merge_format_mode) {#str_strlist_saveformat_mergeformatmode}

Merges the given input documents into a single output document using specified input output file names and the final document format.


```python
def merge(self, output_file: str, input_files: List[str], save_format: aspose.words.SaveFormat, merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_file | str |  |
| input_files | List[str] |  |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) |  |

## merge(output_file, input_files, save_options, merge_format_mode) {#str_strlist_saveoptions_mergeformatmode}

Merges the given input documents into a single output document using specified input output file names and save options.


```python
def merge(self, output_file: str, input_files: List[str], save_options: aspose.words.saving.SaveOptions, merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_file | str |  |
| input_files | List[str] |  |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) |  |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) |  |

## merge(input_files, merge_format_mode) {#strlist_mergeformatmode}

Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document.



```python
def merge(self, input_files: List[str], merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_files | List[str] |  |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) |  |

## merge(output_stream, input_streams, save_format) {#bytesio_bytesiolist_saveformat}

Merges the given input documents into a single output document using specified input output streams and the final document format.


```python
def merge(self, output_stream: BytesIO, input_streams: List[BytesIO], save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | BytesIO |  |
| input_streams | List[BytesIO] |  |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## merge(output_stream, input_streams, save_options, merge_format_mode) {#bytesio_bytesiolist_saveoptions_mergeformatmode}

Merges the given input documents into a single output document using specified input output streams and save options.


```python
def merge(self, output_stream: BytesIO, input_streams: List[BytesIO], save_options: aspose.words.saving.SaveOptions, merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | BytesIO |  |
| input_streams | List[BytesIO] |  |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) |  |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) |  |

## merge(input_streams, merge_format_mode) {#bytesiolist_mergeformatmode}

Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document.



```python
def merge(self, input_streams: List[BytesIO], merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_streams | List[BytesIO] |  |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) |  |

## See Also

* module [aspose.words.lowcode](../../)
* class [Merger](../)

