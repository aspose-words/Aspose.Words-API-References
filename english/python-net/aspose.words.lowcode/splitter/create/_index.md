---
title: Splitter.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Python
description: "Splitter.create method. Creates new instance of the splitter processor."
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/splitter/create/
---

## create(context) {#splittercontext}

Creates new instance of the splitter processor.


```python
def create(self, context: aspose.words.lowcode.SplitterContext):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| context | [SplitterContext](../../splittercontext/) |  |

### Examples

Shows how to split document by pages using context.

```python
doc = MY_DIR + 'Big document.docx'
splitter_context = aw.lowcode.SplitterContext()
splitter_context.split_options.split_criteria = aw.lowcode.SplitCriteria.PAGE
aw.lowcode.Splitter.create(splitter_context).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.SplitContextDocument.docx').execute()
```

### See Also

* module [aspose.words.lowcode](../../)
* class [Splitter](../)

