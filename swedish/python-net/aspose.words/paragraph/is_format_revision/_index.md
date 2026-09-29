---
title: Paragraph.is_format_revision property
linktitle: is_format_revision property
articleTitle: is_format_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_format_revision property. Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled."
type: docs
weight: 90
url: /sv/python-net/aspose.words/paragraph/is_format_revision/
---

## Paragraph.is_format_revision property

Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.


```python
@property
def is_format_revision(self) -> bool:
    ...

```

### Examples

Shows how to check whether a paragraph is a format revision.

```python
doc = aw.Document(file_name=MY_DIR + 'Format revision.docx')
# Detta stycke är en \"Format\"-revision, som uppstår när vi ändrar formateringen av befintlig text
# medan vi spårar revisioner i Microsoft Word via "Review" -> "Track changes".
self.assertTrue(doc.first_section.body.first_paragraph.is_format_revision)
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

