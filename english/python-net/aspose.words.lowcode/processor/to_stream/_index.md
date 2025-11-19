---
title: Processor.to_stream method
linktitle: to_stream method
articleTitle: to_stream method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Processor.to_stream method"
type: docs
weight: 50
url: /python-net/aspose.words.lowcode/processor/to_stream/
---

## to_stream(output, save_options) {#bytesio_saveoptions}

Specifies output stream for the processor.


```python
def to_stream(self, output: io.BytesIO, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output | io.BytesIO | Output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Save options. |

### Remarks

If the output consists of multiple files, only the first part will be saved to the specified stream.


### Returns

Returns processor with specified output stream.


## to_stream(output, save_format) {#bytesio_saveformat}

Specifies output stream for the processor.


```python
def to_stream(self, output: io.BytesIO, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output | io.BytesIO | Output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. |

### Remarks

If the output consists of multiple files, only the first part will be saved to the specified stream.


### Returns

Returns processor with specified output stream.


## Examples

Shows how to merge documents from stream into a single output document using context.

```python
#There is a several ways to merge documents:
input_doc1 = MY_DIR + 'Big document.docx'
input_doc2 = MY_DIR + 'Tables.docx'
with system_helper.io.FileStream(MY_DIR + 'Big document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as first_stream_in:
    with system_helper.io.FileStream(MY_DIR + 'Tables.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as second_stream_in:
        save_options = aw.saving.OoxmlSaveOptions()
        save_options.password = 'Aspose.Words'
        with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.MergeStreamContextDocuments.1.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
            context = aw.lowcode.MergerContext()
            context.merge_format_mode = aw.lowcode.MergeFormatMode.KEEP_SOURCE_FORMATTING
            aw.lowcode.Merger.create(context).from_stream(input=first_stream_in).from_stream(input=second_stream_in).to_stream(output=stream_out, save_options=save_options).execute()
        first_load_options = aw.loading.LoadOptions()
        first_load_options.ignore_ole_data = True
        second_load_options = aw.loading.LoadOptions()
        second_load_options.ignore_ole_data = False
        with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.MergeStreamContextDocuments.2.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
            context2 = aw.lowcode.MergerContext()
            context2.merge_format_mode = aw.lowcode.MergeFormatMode.KEEP_SOURCE_FORMATTING
            aw.lowcode.Merger.create(context2).from_stream(input=first_stream_in, load_options=first_load_options).from_stream(input=second_stream_in, load_options=second_load_options).to_stream(output=stream_out, save_format=aw.SaveFormat.DOCX).execute()
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Processor](../)

