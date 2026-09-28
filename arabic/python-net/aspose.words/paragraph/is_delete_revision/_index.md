---
title: Paragraph.is_delete_revision property
linktitle: is_delete_revision property
articleTitle: is_delete_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_delete_revision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 40
url: /ar/python-net/aspose.words/paragraph/is_delete_revision/
---

## Paragraph.is_delete_revision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.


```python
@property
def is_delete_revision(self) -> bool:
    ...

```

### Examples

Shows how to work with revision paragraphs.

```python
doc = aw.Document()
body = doc.first_section.body
para = body.first_paragraph
para.append_child(aw.Run(doc=doc, text='Paragraph 1. '))
body.append_paragraph('Paragraph 2. ')
body.append_paragraph('Paragraph 3. ')
# الفقرات المذكورة أعلاه ليست مراجعات.
# الفقرات التي نضيفها بعد بدء تتبع المراجعات ستُسجل كمراجعات \"إدراج\".
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
para = body.append_paragraph('Paragraph 4. ')
self.assertTrue(para.is_insert_revision)
# الفقرات التي نزيلها بعد بدء تتبع المراجعات ستُسجل كمراجعات \"حذف\".
paragraphs = body.paragraphs
self.assertEqual(4, paragraphs.count)
para = paragraphs[2]
para.remove()
# ستظل هذه الفقرات موجودة حتى نقبل أو نرفض مراجعة الحذف.
# قبول المراجعة سيزيل الفقرة نهائيًا،
# ورفض المراجعة سيتركها في المستند كما لو لم نحذفها أبدًا.
self.assertEqual(4, paragraphs.count)
self.assertTrue(para.is_delete_revision)
# اقبل المراجعة، ثم تحقق من أن الفقرة اختفت.
doc.accept_all_revisions()
self.assertEqual(3, paragraphs.count)
self.assertEqual(0, para.count)
self.assertEqual('Paragraph 1. \r' + 'Paragraph 2. \r' + 'Paragraph 4.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

