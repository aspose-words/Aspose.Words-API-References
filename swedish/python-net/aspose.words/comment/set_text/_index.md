---
title: Comment.set_text method
linktitle: set_text method
articleTitle: set_text method
second_title: Aspose.Words for Python
description: "Comment.set_text method. This is a convenience method that allows to easily set text of the comment."
type: docs
weight: 190
url: /sv/python-net/aspose.words/comment/set_text/
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
# Placera kommentaren vid en nod i dokumentets kropp.
# Denna kommentar kommer att visas vid platsen för dess stycke,
# utanför sidans högermarginal, och med en prickad linje som kopplar den till dess stycke.
builder.current_paragraph.append_child(comment)
# Lägg till ett svar som visas under dess föräldrakommentar.
comment.add_reply('Joe Bloggs', 'J.B.', datetime.datetime.now(), 'New reply')
# Kommentarer och svar är båda Kommentar-noder.
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.COMMENT, True).count)
# Kommentarer som inte svarar på andra kommentarer är "top-level". De har inga föräldrakommentarer.
self.assertIsNone(comment.ancestor)
# Svar har en överordnad top-level-kommentar.
self.assertEqual(comment, comment.replies[0].ancestor)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.AddCommentWithReply.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

