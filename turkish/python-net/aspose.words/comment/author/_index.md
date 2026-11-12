---
title: Comment.author property
linktitle: author property
articleTitle: author property
second_title: Aspose.Words for Python
description: "Comment.author property. Returns or sets the author name for a comment."
type: docs
weight: 30
url: /tr/python-net/aspose.words/comment/author/
---

## Comment.author property

Returns or sets the author name for a comment.


```python
@property
def author(self) -> str:
    ...

@author.setter
def author(self, value: str):
    ...

```

### Remarks

Cannot be ``None``.

Default is empty string.




### Examples

Shows how to print all of a document's comments and their replies.

```python
doc = aw.Document(file_name=MY_DIR + 'Comments.docx')
comments = doc.get_child_nodes(aw.NodeType.COMMENT, True)
# Bir yorumun üst öğesi yoksa, bu bir "üst düzey" yorumdur, yanıt türündeki bir yorumun aksine.
# Tüm üst düzey yorumları ve varsa yanıtlarını yazdırın.
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

