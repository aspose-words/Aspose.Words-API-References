---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words for .NET
description: Effortlessly clear all replies to your comment with the RemoveAllReplies method, ensuring a clutter-free discussion and enhanced user experience.
type: docs
weight: 170
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

* class [Comment](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
