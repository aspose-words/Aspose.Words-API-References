---
title: Paragraph.is_format_revision property
linktitle: is_format_revision property
articleTitle: is_format_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_format_revision property. Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled."
type: docs
weight: 90
url: /zh/python-net/aspose.words/paragraph/is_format_revision/
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
# 此段落是一次 "Format" 修订，当我们更改现有文本的格式时会产生此修订
# 在 Microsoft Word 中通过 "Review" -> "Track changes" 跟踪修订时。
self.assertTrue(doc.first_section.body.first_paragraph.is_format_revision)
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

