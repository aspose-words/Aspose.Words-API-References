---
title: ParagraphFormat.mirror_indents property
linktitle: mirror_indents property
articleTitle: mirror_indents property
second_title: Aspose.Words for Python
description: "ParagraphFormat.mirror_indents property. Gets or sets a flag indicating whether the left and right indents are of the same width."
type: docs
weight: 240
url: /python-net/aspose.words/paragraphformat/mirror_indents/
---

## ParagraphFormat.mirror_indents property

Gets or sets a flag indicating whether the left and right indents are of the same width.


```python
@property
def mirror_indents(self) -> bool:
    ...

@mirror_indents.setter
def mirror_indents(self, value: bool):
    ...

```

### Examples

Show how to make left and right indents the same.

```python
doc = aw.Document(file_name=MY_DIR + "Document.docx")
format = doc.first_section.body.paragraphs[0].paragraph_format
format.mirror_indents = True
doc.save(file_name=ARTIFACTS_DIR + "ParagraphFormat.MirrorIndents.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

