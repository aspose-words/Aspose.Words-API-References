---
title: Comment.replies property
linktitle: replies property
articleTitle: replies property
second_title: Aspose.Words for Python
description: "Comment.replies property. Returns a collection of [Comment](../) objects that are immediate children of the specified comment."
type: docs
weight: 110
url: /ar/python-net/aspose.words/comment/replies/
---

## Comment.replies property

Returns a collection of [Comment](../) objects that are immediate children of the specified comment.



```python
@property
def replies(self) -> aspose.words.CommentCollection:
    ...

```

### Examples

Shows how to print all of a document's comments and their replies.

```python
doc = aw.Document(file_name=MY_DIR + 'Comments.docx')
comments = doc.get_child_nodes(aw.NodeType.COMMENT, True)
# إذا كان التعليق لا يحتوي على سلف، فهو تعليق "مستوى أعلى" على عكس التعليق من نوع الرد.
# اطبع جميع التعليقات ذات المستوى الأعلى مع أي ردود قد تكون لديها.
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

