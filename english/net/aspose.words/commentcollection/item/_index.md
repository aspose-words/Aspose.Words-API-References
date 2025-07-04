---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access specific comments effortlessly with the CommentCollection Item property. Retrieve comments by index for streamlined content management.
type: docs
weight: 10
url: /net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Retrieves a [`Comment`](../../comment/) at the given index.

```csharp
public Comment this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | An index into the collection. |

## Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples

Shows how to remove comment replies.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.That(comment.Replies.Count, Is.EqualTo(2)); 

// Below are two ways of removing replies from a comment.
// 1 -  Use the "RemoveReply" method to remove replies from a comment individually:
comment.RemoveReply(comment.Replies[0]);

Assert.That(comment.Replies.Count, Is.EqualTo(1));

// 2 -  Use the "RemoveAllReplies" method to remove all replies from a comment at once:
comment.RemoveAllReplies();

Assert.That(comment.Replies.Count, Is.EqualTo(0));
```

### See Also

* class [Comment](../../comment/)
* class [CommentCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
