---
title: Comment.set_text method
linktitle: set_text method
articleTitle: set_text method
second_title: Aspose.Words for Python
description: "Comment.set_text method. This is a convenience method that allows to easily set text of the comment."
type: docs
weight: 190
url: /fr/python-net/aspose.words/comment/set_text/
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
# Placez le commentaire sur un nœud dans le corps du document.
# Ce commentaire apparaîtra à l'emplacement de son paragraphe,
# en dehors de la marge droite de la page, et avec une ligne pointillée le reliant à son paragraphe.
builder.current_paragraph.append_child(comment)
# Ajoutez une réponse, qui apparaîtra sous le commentaire parent.
comment.add_reply('Joe Bloggs', 'J.B.', datetime.datetime.now(), 'New reply')
# Les commentaires et les réponses sont tous deux des nœuds Comment.
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.COMMENT, True).count)
# Les commentaires qui ne répondent pas à d'autres commentaires sont "top-level". Ils n'ont aucun commentaire ancêtre.
self.assertIsNone(comment.ancestor)
# Les réponses ont un commentaire ancêtre top-level.
self.assertEqual(comment, comment.replies[0].ancestor)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.AddCommentWithReply.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

