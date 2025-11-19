---
title: Processor.from_stream method
linktitle: from_stream method
articleTitle: from_stream method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Processor.from_stream method"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/processor/from_stream/
---

## from_stream(input) {#bytesio}

Specifies input document for processing.


```python
def from_stream(self, input: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input | io.BytesIO | Input document stream. |

### Remarks

If the processor accepts only one file as an input, only the last specified file will be processed.
[Merger](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged.
[Converter](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted. 



### Returns

Returns processor with specified input file stream.


## from_stream(input, load_options) {#bytesio_loadoptions}

Specifies input document for processing.


```python
def from_stream(self, input: io.BytesIO, load_options: aspose.words.loading.LoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input | io.BytesIO | Input document stream. |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) | Optional load options used to load the document. |

### Remarks

If the processor accepts only one file as an input, only the last specified file will be processed.
[Merger](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged.
[Converter](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted. 



### Returns

Returns processor with specified input file stream.


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

