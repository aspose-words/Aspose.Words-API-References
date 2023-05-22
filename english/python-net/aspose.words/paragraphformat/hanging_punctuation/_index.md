---
title: ParagraphFormat.hanging_punctuation property
linktitle: hanging_punctuation property
articleTitle: hanging_punctuation property
second_title: Aspose.Words for Python
description: "ParagraphFormat.hanging_punctuation property. Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph."
type: docs
weight: 120
url: /python-net/aspose.words/paragraphformat/hanging_punctuation/
---

## ParagraphFormat.hanging_punctuation property

Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph.


### Examples

Shows how to set special properties for Asian typography.

```python
doc = aw.Document(MY_DIR + "Document.docx")

format = doc.first_section.body.first_paragraph.paragraph_format
format.far_east_line_break_control = True
format.word_wrap = False
format.hanging_punctuation = True

doc.save(ARTIFACTS_DIR + "ParagraphFormat.asian_typography_properties.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

