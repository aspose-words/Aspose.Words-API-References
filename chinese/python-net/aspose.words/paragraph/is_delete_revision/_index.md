---
title: Paragraph.is_delete_revision property
linktitle: is_delete_revision property
articleTitle: is_delete_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_delete_revision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 40
url: /zh/python-net/aspose.words/paragraph/is_delete_revision/
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
# 上述段落不是修订。
# 在开始修订跟踪后添加的段落将记录为 "Insert" 修订。
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
para = body.append_paragraph('Paragraph 4. ')
self.assertTrue(para.is_insert_revision)
# 在开始修订跟踪后删除的段落将记录为 "Delete" 修订。
paragraphs = body.paragraphs
self.assertEqual(4, paragraphs.count)
para = paragraphs[2]
para.remove()
# 此类段落将保留，直到我们接受或拒绝删除修订。
# 接受修订将永久删除该段落，
# 而拒绝修订则会让它保留在文档中，好像我们从未删除过它。
self.assertEqual(4, paragraphs.count)
self.assertTrue(para.is_delete_revision)
# 接受修订，然后验证该段落已消失。
doc.accept_all_revisions()
self.assertEqual(3, paragraphs.count)
self.assertEqual(0, para.count)
self.assertEqual('Paragraph 1. \r' + 'Paragraph 2. \r' + 'Paragraph 4.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

