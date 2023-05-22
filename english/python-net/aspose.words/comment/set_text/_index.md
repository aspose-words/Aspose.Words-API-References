---
title: Comment.set_text method
linktitle: set_text method
articleTitle: set_text method
second_title: Aspose.Words for Python
description: "Comment.set_text method. This is a convenience method that allows to easily set text of the comment."
type: docs
weight: 150
url: /python-net/aspose.words/comment/set_text/
---

## set_text(text) {#str}

This is a convenience method that allows to easily set text of the comment.


```python
def set_text(self, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | str |  |

This method allows to quickly set text of a comment from a string. The string can contain
paragraph breaks, this will create paragraphs of text in the comment accordingly.
If you want to insert more complex elements into the comment, for example bookmarks
or tables or apply rich formatting, then you need to use the appropriate node classes to 
build up the comment text.




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

