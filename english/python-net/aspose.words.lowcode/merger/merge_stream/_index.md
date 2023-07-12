---
title: Merger.merge_stream method
linktitle: merge_stream method
articleTitle: merge_stream method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Merger.merge_stream method"
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/merger/merge_stream/
---

## merge_stream(output_stream, input_streams, save_format) {#bytesio_bytesiolist_saveformat}

Merges the given input documents into a single output document using specified input output streams and the final document format.


```python
def merge_stream(self, output_stream: BytesIO, input_streams: List[BytesIO], save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | BytesIO |  |
| input_streams | List[BytesIO] |  |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## merge_stream(output_stream, input_streams, save_options, merge_format_mode) {#bytesio_bytesiolist_saveoptions_mergeformatmode}

Merges the given input documents into a single output document using specified input output streams and save options.


```python
def merge_stream(self, output_stream: BytesIO, input_streams: List[BytesIO], save_options: aspose.words.saving.SaveOptions, merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | BytesIO |  |
| input_streams | List[BytesIO] |  |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) |  |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) |  |

## merge_stream(input_streams, merge_format_mode) {#bytesiolist_mergeformatmode}

Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document.



```python
def merge_stream(self, input_streams: List[BytesIO], merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_streams | List[BytesIO] |  |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) |  |

## See Also

* module [aspose.words.lowcode](../../)
* class [Merger](../)

