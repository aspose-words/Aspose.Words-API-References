---
title: Paragraph.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 110
url: /tr/python-net/aspose.words/paragraph/is_insert_revision/
---

## Paragraph.is_insert_revision property

Returns true if this object was inserted in Microsoft Word while change tracking was enabled.


```python
@property
def is_insert_revision(self) -> bool:
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
# Yukarıdaki paragraflar revizyon değildir.
# Revizyon takibini başlattıktan sonra eklediğimiz paragraflar \"Insert\" revizyonu olarak kaydedilir.
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
para = body.append_paragraph('Paragraph 4. ')
self.assertTrue(para.is_insert_revision)
# Revizyon takibini başlattıktan sonra sildiğimiz paragraflar \"Delete\" revizyonu olarak kaydedilir.
paragraphs = body.paragraphs
self.assertEqual(4, paragraphs.count)
para = paragraphs[2]
para.remove()
# Bu paragraflar, silme revizyonunu kabul edene veya reddedene kadar kalır.
# Revizyonu kabul etmek paragrafı kalıcı olarak kaldırır,
# ve revizyonu reddetmek, sanki hiç silinmemiş gibi belge içinde bırakır.
self.assertEqual(4, paragraphs.count)
self.assertTrue(para.is_delete_revision)
# Revizyonu kabul edin ve ardından paragrafın kaybolduğunu doğrulayın.
doc.accept_all_revisions()
self.assertEqual(3, paragraphs.count)
self.assertEqual(0, para.count)
self.assertEqual('Paragraph 1. \r' + 'Paragraph 2. \r' + 'Paragraph 4.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

