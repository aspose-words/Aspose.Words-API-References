---
title: Processor.to_file method
linktitle: to_file method
articleTitle: to_file method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Processor.to_file method"
type: docs
weight: 40
url: /python-net/aspose.words.lowcode/processor/to_file/
---

## to_file(output) {#str}

Specifies output file for the processor.


```python
def to_file(self, output: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output | str | Output file name. |

### Remarks

If the output consists of multiple files, the specified output file name is used to generate the file name
for each part following the rule: 'outputFile_partIndex.extension'.


### Returns

Returns processor with specified output file.


## to_file(output, save_options) {#str_saveoptions}

Specifies output file for the processor.


```python
def to_file(self, output: str, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output | str | Output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Optional save options. If not specified, save format is determined by the file extension. |

### Remarks

If the output consists of multiple files, the specified output file name is used to generate the file name
for each part following the rule: 'outputFile_partIndex.extension'.


### Returns

Returns processor with specified output file.


## to_file(output, save_format) {#str_saveformat}

Specifies output file for the processor.


```python
def to_file(self, output: str, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output | str | Output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Save format. If not specified, save format is determined by the file extension. |

### Remarks

If the output consists of multiple files, the specified output file name is used to generate the file name
for each part following the rule: 'outputFile_partIndex.extension'.


### Returns

Returns processor with specified output file.


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

