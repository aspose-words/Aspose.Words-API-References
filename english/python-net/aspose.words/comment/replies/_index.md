---
title: Comment.replies property
linktitle: replies property
articleTitle: replies property
second_title: Aspose.Words for Python
description: "Comment.replies property. Returns a collection of [Comment](../) objects that are immediate children of the specified comment."
type: docs
weight: 100
url: /python-net/aspose.words/comment/replies/
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
doc = aw.Document(MY_DIR + "Comments.docx")

comments = doc.get_child_nodes(aw.NodeType.COMMENT, True)

# If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
# Print all top-level comments along with any replies they may have.
for comment in comments:
    comment = comment.as_comment()
    if comment.ancestor is None:
        print("Top-level comment:")
        print(f"\t\"{comment.get_text().strip()}\", by {comment.author}")
        print(f"Has {comment.replies.count} replies")
        for comment_reply in comment.replies:
            comment_reply = comment_reply.as_comment()
            print(f"\t\"{comment_reply.get_text().strip()}\", by {comment_reply.author}")
        print()
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

