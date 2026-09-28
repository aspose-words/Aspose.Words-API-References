---
title: Comment.ancestor property
linktitle: ancestor property
articleTitle: ancestor property
second_title: Aspose.Words for Python
description: "Comment.ancestor property. Returns the parent [Comment](../) object"
type: docs
weight: 20
url: /zh/python-net/aspose.words/comment/ancestor/
---

## Comment.ancestor property

Returns the parent [Comment](../) object. Returns ``None`` for top-level comments.



```python
@property
def ancestor(self) -> aspose.words.Comment:
    ...

```

### Examples

Shows how to print all of a document's comments and their replies.

```python
doc = aw.Document(file_name=MY_DIR + 'Comments.docx')
comments = doc.get_child_nodes(aw.NodeType.COMMENT, True)
# 如果评论没有祖先，它就是一个“顶级”评论，而不是回复类型的评论。
# 打印所有顶级评论以及它们可能拥有的任何回复。
for comment in list(filter(lambda c: c.ancestor == None, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_comment(), b), list(comments)))))):
    print('Top-level comment:')
    print(f'\t"{comment.get_text().strip()}", by {comment.author}')
    print(f'Has {comment.replies.count} replies')
    for comment_reply in comment.replies:
        comment_reply = comment_reply.as_comment()
        print(f'\t"{comment_reply.get_text().strip()}", by {comment_reply.author}')
    print()
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

