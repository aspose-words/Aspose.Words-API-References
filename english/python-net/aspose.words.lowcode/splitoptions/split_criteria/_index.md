---
title: SplitOptions.split_criteria property
linktitle: split_criteria property
articleTitle: split_criteria property
second_title: Aspose.Words for Python
description: "SplitOptions.split_criteria property. Specifies the criteria for splitting the document into parts."
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/splitoptions/split_criteria/
---

## SplitOptions.split_criteria property

Specifies the criteria for splitting the document into parts.


```python
@property
def split_criteria(self) -> aspose.words.lowcode.SplitCriteria:
    ...

@split_criteria.setter
def split_criteria(self, value: aspose.words.lowcode.SplitCriteria):
    ...

```

### Examples

Shows how to split document by pages.

```python
doc = MY_DIR + 'Big document.docx'
options = aw.lowcode.SplitOptions()
options.split_criteria = aw.lowcode.SplitCriteria.PAGE
aw.lowcode.Splitter.split(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.SplitDocument.1.docx', options=options)
aw.lowcode.Splitter.split(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.SplitDocument.2.docx', save_format=aw.SaveFormat.DOCX, options=options)
```

### See Also

* module [aspose.words.lowcode](../../)
* class [SplitOptions](../)

