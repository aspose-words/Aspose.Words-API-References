---
title: Comment.set_text method
linktitle: set_text method
articleTitle: set_text method
second_title: Aspose.Words for Python
description: "Comment.set_text method. This is a convenience method that allows to easily set text of the comment."
type: docs
weight: 190
url: /zh/python-net/aspose.words/comment/set_text/
---

## set_text(text) {#str}

This is a convenience method that allows to easily set text of the comment.


```python
def set_text(self, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | str | The new text of the comment. |

### Remarks

This method allows to quickly set text of a comment from a string. The string can contain
paragraph breaks, this will create paragraphs of text in the comment accordingly.
If you want to insert more complex elements into the comment, for example bookmarks
or tables or apply rich formatting, then you need to use the appropriate node classes to
build up the comment text.




### Examples

Shows how to add a comment to a document, and then reply to it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('My comment.')
# 将注释放置在文档正文的节点上。
# 此注释将显示在其段落所在的位置，
# 在页面右侧边距之外，并用虚线将其连接到段落。
builder.current_paragraph.append_child(comment)
# 添加回复，该回复将显示在其父评论下方。
comment.add_reply('Joe Bloggs', 'J.B.', datetime.datetime.now(), 'New reply')
# 评论和回复都是 Comment 节点。
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.COMMENT, True).count)
# 不回复其他评论的评论被称为 "顶级"。它们没有上级评论。
self.assertIsNone(comment.ancestor)
# 回复拥有一个上级顶级评论。
self.assertEqual(comment, comment.replies[0].ancestor)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.AddCommentWithReply.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

