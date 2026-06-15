---
title: SplitterContext.split_options property
linktitle: split_options property
articleTitle: split_options property
second_title: Aspose.Words for Python
description: "SplitterContext.split_options property. Document split options."
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/splittercontext/split_options/
---

## SplitterContext.split_options property

Document split options.


```python
@property
def split_options(self) -> aspose.words.lowcode.SplitOptions:
    ...

```

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

* module [aspose.words.lowcode](../../)
* class [SplitterContext](../)

