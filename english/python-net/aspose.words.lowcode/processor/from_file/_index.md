---
title: Processor.from_file method
linktitle: from_file method
articleTitle: from_file method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Processor.from_file method"
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/processor/from_file/
---

## from_file(input) {#str}

Specifies input document for processing.


```python
def from_file(self, input: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input | str | Input document file name. |

### Remarks

If the processor accepts only one file as an input, only the last specified file will be processed.
[Merger](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged.
[Converter](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted. 



### Returns

Returns processor with specified input file.


## from_file(input, load_options) {#str_loadoptions}

Specifies input document for processing.


```python
def from_file(self, input: str, load_options: aspose.words.loading.LoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input | str | Input document file name. |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) | Optional load options used to load the document. |

### Remarks

If the processor accepts only one file as an input, only the last specified file will be processed.
[Merger](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged.
[Converter](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted. 



### Returns

Returns processor with specified input file.


## Examples

Shows how to merge documents into a single output document using context.

```python
#There is a several ways to merge documents:
input_doc1 = MY_DIR + 'Big document.docx'
input_doc2 = MY_DIR + 'Tables.docx'
context = aw.lowcode.MergerContext()
context.merge_format_mode = aw.lowcode.MergeFormatMode.KEEP_SOURCE_FORMATTING
aw.lowcode.Merger.create(context).from_file(input=input_doc1).from_file(input=input_doc2).to_file(output=ARTIFACTS_DIR + 'LowCode.MergeContextDocuments.1.docx').execute()
first_load_options = aw.loading.LoadOptions()
first_load_options.ignore_ole_data = True
second_load_options = aw.loading.LoadOptions()
second_load_options.ignore_ole_data = False
context2 = aw.lowcode.MergerContext()
context2.merge_format_mode = aw.lowcode.MergeFormatMode.KEEP_SOURCE_FORMATTING
aw.lowcode.Merger.create(context2).from_file(input=input_doc1, load_options=first_load_options).from_file(input=input_doc2, load_options=second_load_options).to_file(output=ARTIFACTS_DIR + 'LowCode.MergeContextDocuments.2.docx', save_format=aw.SaveFormat.DOCX).execute()
save_options = aw.saving.OoxmlSaveOptions()
save_options.password = 'Aspose.Words'
context3 = aw.lowcode.MergerContext()
context3.merge_format_mode = aw.lowcode.MergeFormatMode.KEEP_SOURCE_FORMATTING
aw.lowcode.Merger.create(context3).from_file(input=input_doc1).from_file(input=input_doc2).to_file(output=ARTIFACTS_DIR + 'LowCode.MergeContextDocuments.3.docx', save_options=save_options).execute()
```

Shows how to convert documents with a single line of code using context.

```python
doc = MY_DIR + 'Big document.docx'
aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.ConvertContext.1.pdf').execute()
aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.ConvertContext.2.pdf', save_format=aw.SaveFormat.RTF).execute()
save_options = aw.saving.OoxmlSaveOptions()
save_options.password = 'Aspose.Words'
load_options = aw.loading.LoadOptions()
load_options.ignore_ole_data = True
aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc, load_options=load_options).to_file(output=ARTIFACTS_DIR + 'LowCode.ConvertContext.3.docx', save_options=save_options).execute()
aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.ConvertContext.4.png', save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)).execute()
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Processor](../)

