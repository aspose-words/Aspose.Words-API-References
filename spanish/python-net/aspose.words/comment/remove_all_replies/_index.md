---
title: Comment.remove_all_replies method
linktitle: remove_all_replies method
articleTitle: remove_all_replies method
second_title: Aspose.Words for Python
description: "Comment.remove_all_replies method. Removes all replies to this comment."
type: docs
weight: 170
url: /es/python-net/aspose.words/comment/remove_all_replies/
---

## remove_all_replies() {#default}

Removes all replies to this comment.


```python
def remove_all_replies(self):
    ...
```

### Remarks

All constituent nodes of the replies will be deleted from the document.


### Examples

Shows how to remove comment replies.

```python
doc = aw.Document()
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('My comment.')
doc.first_section.body.first_paragraph.append_child(comment)
comment.add_reply('Joe Bloggs', 'J.B.', datetime.datetime.now(), 'New reply')
comment.add_reply('Joe Bloggs', 'J.B.', datetime.datetime.now(), 'Another reply')
self.assertEqual(2, comment.replies.count)
# A continuación se presentan dos formas de eliminar respuestas de un comentario.
# 1 -  Utilice el método "RemoveReply" para eliminar respuestas de un comentario individualmente:
comment.remove_reply(comment.replies[0])
self.assertEqual(1, comment.replies.count)
# 2 -  Utilice el método "RemoveAllReplies" para eliminar todas las respuestas de un comentario de una vez:
comment.remove_all_replies()
self.assertEqual(0, comment.replies.count)
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

