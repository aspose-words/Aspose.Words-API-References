---
title: ParagraphFormat.baseline_alignment property
linktitle: baseline_alignment property
articleTitle: baseline_alignment property
second_title: Aspose.Words for Python
description: "ParagraphFormat.baseline_alignment property. Gets or sets fonts vertical position on a line."
type: docs
weight: 40
url: /python-net/aspose.words/paragraphformat/baseline_alignment/
---

## ParagraphFormat.baseline_alignment property

Gets or sets fonts vertical position on a line.


```python
@property
def baseline_alignment(self) -> aspose.words.BaselineAlignment:
    ...

@baseline_alignment.setter
def baseline_alignment(self, value: aspose.words.BaselineAlignment):
    ...

```

### Examples

Shows how to set fonts vertical position on a line.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
format = doc.first_section.body.paragraphs[0].paragraph_format
if format.baseline_alignment == aw.BaselineAlignment.AUTO:
    format.baseline_alignment = aw.BaselineAlignment.TOP
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphBaselineAlignment.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

