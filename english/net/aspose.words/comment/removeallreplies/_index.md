---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words for .NET
description: Comment RemoveAllReplies method. Removes all replies to this comment in C#.
type: docs
weight: 160
url: /net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Removes all replies to this comment.

```csharp
public void RemoveAllReplies()
```

## Remarks

All constituent nodes of the replies will be deleted from the document.

## Examples

Shows how to remove comment replies.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// Below are two ways of removing replies from a comment.
// 1 -  Use the "RemoveReply" method to remove replies from a comment individually:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 -  Use the "RemoveAllReplies" method to remove all replies from a comment at once:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### See Also

* class [Comment](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
