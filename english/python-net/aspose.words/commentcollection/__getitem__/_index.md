---
title: CommentCollection indexer
second_title: Aspose.Words for Python via .NET API Reference
description: "Retrieves a [Comment](../../comment/) at the given index."
type: docs
weight: 10
url: /python-net/aspose.words/commentcollection/__getitem__/
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

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to remove comment replies.

```python
doc = aw.Document()

comment = aw.Comment(doc, "John Doe", "J.D.", datetime.now())
comment.set_text("My comment.")

doc.first_section.body.first_paragraph.append_child(comment)

comment.add_reply("Joe Bloggs", "J.B.", datetime.now(), "New reply")
comment.add_reply("Joe Bloggs", "J.B.", datetime.now(), "Another reply")

self.assertEqual(2, comment.replies.count)

# Below are two ways of removing replies from a comment.
# 1 -  Use the "remove_reply" method to remove replies from a comment individually:
comment.remove_reply(comment.replies[0])

self.assertEqual(1, comment.replies.count)

# 2 -  Use the "remove_all_replies" method to remove all replies from a comment at once:
comment.remove_all_replies()

self.assertEqual(0, comment.replies.count)
```

### See Also

* module [aspose.words](../../)
* class [CommentCollection](../)

