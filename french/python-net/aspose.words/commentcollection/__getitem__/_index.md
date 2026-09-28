---
title: CommentCollection indexer
linktitle: CommentCollection indexer
articleTitle: CommentCollection indexer
second_title: Aspose.Words for Python
description: "CommentCollection indexer. Retrieves a [Comment](../../comment/) at the given index."
type: docs
weight: 10
url: /fr/python-net/aspose.words/commentcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [Comment](../../comment/) at the given index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




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
# Voici deux méthodes pour supprimer les réponses d'un commentaire.
# 1 -  Utilisez la méthode "RemoveReply" pour supprimer les réponses d'un commentaire individuellement :
comment.remove_reply(comment.replies[0])
self.assertEqual(1, comment.replies.count)
# 2 -  Utilisez la méthode "RemoveAllReplies" pour supprimer toutes les réponses d'un commentaire en une fois :
comment.remove_all_replies()
self.assertEqual(0, comment.replies.count)
```

### See Also

* module [aspose.words](../../)
* class [CommentCollection](../)

