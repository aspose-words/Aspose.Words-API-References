---
title: Processor.execute method
linktitle: execute method
articleTitle: execute method
second_title: Aspose.Words for Python
description: "Processor.execute method. Execute the processor action."
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/processor/execute/
---

## execute() {#default}

Execute the processor action.


```python
def execute(self):
    ...
```

### Examples

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

### See Also

* module [aspose.words.lowcode](../../)
* class [Processor](../)

