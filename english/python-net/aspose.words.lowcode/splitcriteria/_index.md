---
title: SplitCriteria enumeration
linktitle: SplitCriteria enumeration
articleTitle: SplitCriteria enumeration
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.SplitCriteria enumeration. Specifies how the document is split into parts."
type: docs
weight: 100
url: /python-net/aspose.words.lowcode/splitcriteria/
---

## SplitCriteria enumeration

Specifies how the document is split into parts.


### Members

| Name | Description |
| --- | --- |
| PAGE | Specifies that the document is split into pages. |
| SECTION_BREAK | Specifies that the document is split into parts at a section break of any type. |
| STYLE | Specifies that the document is split into parts at a paragraph formatted using the style specified in [SplitOptions.split_style](../splitoptions/split_style/). |

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

* module [aspose.words.lowcode](../)

