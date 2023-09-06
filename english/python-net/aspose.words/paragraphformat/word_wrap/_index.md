---
title: ParagraphFormat.word_wrap property
linktitle: word_wrap property
articleTitle: word_wrap property
second_title: Aspose.Words for Python
description: "ParagraphFormat.word_wrap property. If this property is ``False``, Latin text in the middle of a word can be wrapped for the current paragraph"
type: docs
weight: 410
url: /python-net/aspose.words/paragraphformat/word_wrap/
---

## ParagraphFormat.word_wrap property

If this property is ``False``, Latin text in the middle of a word can be wrapped for
the current paragraph. Otherwise Latin text is wrapped by whole words.



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

