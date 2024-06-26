﻿---
title: ParagraphFormat.far_east_line_break_control property
linktitle: far_east_line_break_control property
articleTitle: far_east_line_break_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.far_east_line_break_control property. Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph."
type: docs
weight: 110
url: /python-net/aspose.words/paragraphformat/far_east_line_break_control/
---

## ParagraphFormat.far_east_line_break_control property

Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph.


```python
@property
def far_east_line_break_control(self) -> bool:
    ...

@far_east_line_break_control.setter
def far_east_line_break_control(self, value: bool):
    ...

```

### Examples

Shows how to set special properties for Asian typography.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
format = doc.first_section.body.first_paragraph.paragraph_format
format.far_east_line_break_control = True
format.word_wrap = False
format.hanging_punctuation = True
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.AsianTypographyProperties.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

