---
title: Merger.merge_stream method
linktitle: merge_stream method
articleTitle: merge_stream method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Merger.merge_stream method"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/merger/merge_stream/
---

## merge_stream(input_streams, merge_format_mode) {#bytesiolist_mergeformatmode}

Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document.



```python
def merge_stream(self, input_streams: List[io.BytesIO], merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_streams | List[io.BytesIO] | The input streams. |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) | Specifies how to merge formatting that clashes. |

## merge_stream(output_stream, input_streams, save_format) {#bytesio_bytesiolist_saveformat}

Merges the given input documents into a single output document using specified input output streams and the final document format.


```python
def merge_stream(self, output_stream: io.BytesIO, input_streams: List[io.BytesIO], save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | io.BytesIO | The output stream. |
| input_streams | List[io.BytesIO] | The input streams. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |

## merge_stream(output_stream, input_streams, save_options, merge_format_mode) {#bytesio_bytesiolist_saveoptions_mergeformatmode}

Merges the given input documents into a single output document using specified input output streams and save options.


```python
def merge_stream(self, output_stream: io.BytesIO, input_streams: List[io.BytesIO], save_options: aspose.words.saving.SaveOptions, merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | io.BytesIO | The output stream. |
| input_streams | List[io.BytesIO] | The input streams. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) | Specifies how to merge formatting that clashes. |

## merge_stream(output_stream, input_streams, load_options, save_options, merge_format_mode) {#bytesio_bytesiolist_loadoptionslist_saveoptions_mergeformatmode}

Merges the given input documents into a single output document using specified input output streams and save options.


```python
def merge_stream(self, output_stream: io.BytesIO, input_streams: List[io.BytesIO], load_options: List[aspose.words.loading.LoadOptions], save_options: aspose.words.saving.SaveOptions, merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | io.BytesIO | The output stream. |
| input_streams | List[io.BytesIO] | The input streams. |
| load_options | List[[LoadOptions](../../../aspose.words.loading/loadoptions/)] | Load options for the input files. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents from stream into a single output document.

```python
#There is a several ways to merge documents from stream:
with system_helper.io.FileStream(MY_DIR + 'Big document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as first_stream_in:
    with system_helper.io.FileStream(MY_DIR + 'Tables.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as second_stream_in:
        save_options = aw.saving.OoxmlSaveOptions()
        save_options.password = 'Aspose.Words'
        with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.MergeStreamDocument.1.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
            aw.lowcode.Merger.merge_stream(output_stream=stream_out, input_streams=[first_stream_in, second_stream_in], save_options=save_options, merge_format_mode=aw.lowcode.MergeFormatMode.KEEP_SOURCE_FORMATTING)
        with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.MergeStreamDocument.2.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
            aw.lowcode.Merger.merge_stream(output_stream=stream_out, input_streams=[first_stream_in, second_stream_in], save_format=aw.SaveFormat.DOCX)
        first_load_options = aw.loading.LoadOptions()
        first_load_options.ignore_ole_data = True
        second_load_options = aw.loading.LoadOptions()
        second_load_options.ignore_ole_data = False
        with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.MergeStreamDocument.3.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
            aw.lowcode.Merger.merge_stream(output_stream=stream_out, input_streams=[first_stream_in, second_stream_in], load_options=[first_load_options, second_load_options], save_options=save_options, merge_format_mode=aw.lowcode.MergeFormatMode.KEEP_SOURCE_FORMATTING)
        first_doc = aw.lowcode.Merger.merge_stream(input_streams=[first_stream_in, second_stream_in], merge_format_mode=aw.lowcode.MergeFormatMode.MERGE_FORMATTING)
        first_doc.save(file_name=ARTIFACTS_DIR + 'LowCode.MergeStreamDocument.4.docx')
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Merger](../)

