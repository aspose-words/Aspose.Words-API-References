---
title: Comment.remove_reply method
linktitle: remove_reply method
articleTitle: remove_reply method
second_title: Aspose.Words for Python
description: "Comment.remove_reply method. Removes the specified reply to this comment."
type: docs
weight: 180
url: /zh/python-net/aspose.words/comment/remove_reply/
---

## remove_reply(reply) {#comment}

Removes the specified reply to this comment.


```python
def remove_reply(self, reply: aspose.words.Comment):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| reply | [Comment](../) | The comment node of the deleting reply. |

### Remarks

All constituent nodes of the reply will be deleted from the document.


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
# 下面是两种从评论中删除回复的方法。
# 1 - 使用 “RemoveReply” 方法逐个删除评论中的回复：
comment.remove_reply(comment.replies[0])
self.assertEqual(1, comment.replies.count)
# 2 - 使用 “RemoveAllReplies” 方法一次性删除评论中的所有回复：
comment.remove_all_replies()
self.assertEqual(0, comment.replies.count)
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

