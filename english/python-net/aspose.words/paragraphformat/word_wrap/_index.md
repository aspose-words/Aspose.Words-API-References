---
title: ParagraphFormat.word_wrap property
linktitle: word_wrap property
articleTitle: word_wrap property
second_title: Aspose.Words for Python
description: "ParagraphFormat.word_wrap property. If this property is ``False``, Latin text in the middle of a word can be wrapped for the current paragraph"
type: docs
weight: 420
url: /python-net/aspose.words/paragraphformat/word_wrap/
---

## ParagraphFormat.word_wrap property

If this property is ``False``, Latin text in the middle of a word can be wrapped for
the current paragraph. Otherwise Latin text is wrapped by whole words.



```python
@property
def word_wrap(self) -> bool:
    ...

@word_wrap.setter
def word_wrap(self, value: bool):
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

