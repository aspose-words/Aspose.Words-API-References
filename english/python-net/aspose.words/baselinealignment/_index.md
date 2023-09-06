---
title: BaselineAlignment enumeration
linktitle: BaselineAlignment enumeration
articleTitle: BaselineAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.BaselineAlignment enumeration. Specifies fonts vertical position on a line."
type: docs
weight: 20
url: /python-net/aspose.words/baselinealignment/
---

## BaselineAlignment enumeration

Specifies fonts vertical position on a line.


### Members

| Name | Description |
| --- | --- |
| TOP | Aligns along the top of each font. |
| CENTER | Aligns the center points of each font. |
| BASELINE | Aligns to the baseline of the paragraph. |
| BOTTOM | Aligns to the bottom of each font. |
| AUTO | Baseline is adjusted automatically. |

### Examples

Shows how to set fonts vertical position on a line.

```python
doc = aw.Document(MY_DIR + "Office math.docx")

format_ = doc.first_section.body.paragraphs[0].paragraph_format

if format_.baseline_alignment == aw.BaselineAlignment.AUTO:
    format_.baseline_alignment = aw.BaselineAlignment.TOP

doc.save(ARTIFACTS_DIR + "ParagraphFormat.ParagraphBaselineAlignment.docx")
```

### See Also

* module [aspose.words](../)

