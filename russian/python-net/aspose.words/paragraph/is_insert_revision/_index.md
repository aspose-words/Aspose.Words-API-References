---
title: Paragraph.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 110
url: /ru/python-net/aspose.words/paragraph/is_insert_revision/
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
# Вышеуказанные абзацы не являются ревизиями.
# Абзацы, которые мы добавляем после начала отслеживания ревизий, будут зарегистрированы как ревизии типа \"Insert\".
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
para = body.append_paragraph('Paragraph 4. ')
self.assertTrue(para.is_insert_revision)
# Абзацы, которые мы удаляем после начала отслеживания ревизий, будут зарегистрированы как ревизии типа \"Delete\".
paragraphs = body.paragraphs
self.assertEqual(4, paragraphs.count)
para = paragraphs[2]
para.remove()
# Такие абзацы останутся, пока мы не примем или не отклоним ревизию удаления.
# Принятие ревизии окончательно удалит абзац,
# а отклонение ревизии оставит его в документе, как будто мы его никогда не удаляли.
self.assertEqual(4, paragraphs.count)
self.assertTrue(para.is_delete_revision)
# Примите ревизию, а затем проверьте, что абзац исчез.
doc.accept_all_revisions()
self.assertEqual(3, paragraphs.count)
self.assertEqual(0, para.count)
self.assertEqual('Paragraph 1. \r' + 'Paragraph 2. \r' + 'Paragraph 4.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

