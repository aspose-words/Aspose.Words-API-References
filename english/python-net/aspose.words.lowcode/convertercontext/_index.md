---
title: ConverterContext class
linktitle: ConverterContext class
articleTitle: ConverterContext class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.ConverterContext class. Document converter context"
type: docs
weight: 40
url: /python-net/aspose.words.lowcode/convertercontext/
---

## ConverterContext class

Document converter context


**Inheritance:** [ConverterContext](./) → [ProcessorContext](../processorcontext/)

### Constructors
| Name | Description |
| --- | --- |
| [ConverterContext()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [font_settings](../processorcontext/font_settings/) | Font settings used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [layout_options](../processorcontext/layout_options/) | Document layout options used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [warning_callback](../processorcontext/warning_callback/) | Warning callback used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |

### Examples

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

Shows how to convert documents from a stream with a single line of code using context.

```python
doc = MY_DIR + 'Document.docx'
with system_helper.io.FileStream(MY_DIR + 'Big document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.ConvertContextStream.1.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_stream(input=stream_in).to_stream(output=stream_out, save_format=aw.SaveFormat.RTF).execute()
    save_options = aw.saving.OoxmlSaveOptions()
    save_options.password = 'Aspose.Words'
    load_options = aw.loading.LoadOptions()
    load_options.ignore_ole_data = True
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.ConvertContextStream.2.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_stream(input=stream_in, load_options=load_options).to_stream(output=stream_out, save_options=save_options).execute()
    pages = []
    aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc).to_streams(output=pages, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)).execute()
```

### See Also

* module [aspose.words.lowcode](../)
* class [ProcessorContext](../processorcontext/)

