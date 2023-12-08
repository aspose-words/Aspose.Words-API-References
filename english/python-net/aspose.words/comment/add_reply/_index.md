---
title: Comment.add_reply method
linktitle: add_reply method
articleTitle: add_reply method
second_title: Aspose.Words for Python
description: "Comment.add_reply method. Adds a reply to this comment."
type: docs
weight: 150
url: /python-net/aspose.words/comment/add_reply/
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
builder = aw.DocumentBuilder(doc)

comment = aw.Comment(doc, "John Doe", "J.D.", datetime.now())
comment.set_text("My comment.")

# Place the comment at a node in the document's body.
# This comment will show up at the location of its paragraph,
# outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder.current_paragraph.append_child(comment)

# Add a reply, which will show up under its parent comment.
comment.add_reply("Joe Bloggs", "J.B.", datetime.now(), "New reply")

# Comments and replies are both Comment nodes.
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.COMMENT, True).count)

# Comments that do not reply to other comments are "top-level". They have no ancestor comments.
self.assertIsNone(comment.ancestor)

# Replies have an ancestor top-level comment.
self.assertEqual(comment, comment.replies[0].ancestor)

doc.save(ARTIFACTS_DIR + "Comment.add_comment_with_reply.docx")
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

