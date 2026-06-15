---
title: SplitterContext class
linktitle: SplitterContext class
articleTitle: SplitterContext class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.SplitterContext class. Document splitter context."
type: docs
weight: 230
url: /python-net/aspose.words.lowcode/splittercontext/
---

## SplitterContext class

Document splitter context.


**Inheritance:** [SplitterContext](./) → [ProcessorContext](../processorcontext/)

### Constructors
| Name | Description |
| --- | --- |
| [SplitterContext()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [font_settings](../processorcontext/font_settings/) | Font settings used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [layout_options](../processorcontext/layout_options/) | Document layout options used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [split_options](./split_options/) | Document split options. |
| [warning_callback](../processorcontext/warning_callback/) | Warning callback used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |

### Examples

Shows how to split document by pages using context.

```python
doc = MY_DIR + 'Big document.docx'
splitter_context = aw.lowcode.SplitterContext()
splitter_context.split_options.split_criteria = aw.lowcode.SplitCriteria.PAGE
aw.lowcode.Splitter.create(splitter_context).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.SplitContextDocument.docx').execute()
```

Shows how to split document from the stream by pages using context.

```python
with system_helper.io.FileStream(MY_DIR + 'Big document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    splitter_context = aw.lowcode.SplitterContext()
    splitter_context.split_options.split_criteria = aw.lowcode.SplitCriteria.PAGE
    pages = []
    aw.lowcode.Splitter.create(splitter_context).from_stream(input=stream_in).to_streams(output=pages, save_format=aw.SaveFormat.DOCX).execute()
```

### See Also

* module [aspose.words.lowcode](../)
* class [ProcessorContext](../processorcontext/)

