---
title: Comment.add_reply method
linktitle: add_reply method
articleTitle: add_reply method
second_title: Aspose.Words for Python
description: "Comment.add_reply method. Adds a reply to this comment."
type: docs
weight: 160
url: /ru/python-net/aspose.words/comment/add_reply/
---

## add_reply(author, initial, date_time, text) {#str_str_datetime_str}

Adds a reply to this comment.


```python
def add_reply(self, author: str, initial: str, date_time: datetime.datetime, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | str | The author name for the reply. |
| initial | str | The author initials for the reply. |
| date_time | datetime.datetime | The date and time for the reply. |
| text | str | The reply text. |

### Remarks

Due to the existing MS Office limitations only 1 level of replies is allowed in the document.




### Returns

The created [Comment](../) node for the reply.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throws if this method is called on the existing Reply comment. |

### Examples

Shows how to add a comment to a document, and then reply to it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('My comment.')
# Поместите комментарий в узел тела документа.
# Этот комментарий появится в месте своего абзаца,
# за пределами правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder.current_paragraph.append_child(comment)
# Добавьте ответ, который будет отображаться под его родительским комментарием.
comment.add_reply('Joe Bloggs', 'J.B.', datetime.datetime.now(), 'New reply')
# Комментарии и ответы являются узлами типа Comment.
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.COMMENT, True).count)
# Комментарии, которые не отвечают на другие комментарии, являются «верхнего уровня». У них нет родительских комментариев.
self.assertIsNone(comment.ancestor)
# Ответы имеют в качестве предка комментарий верхнего уровня.
self.assertEqual(comment, comment.replies[0].ancestor)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.AddCommentWithReply.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

