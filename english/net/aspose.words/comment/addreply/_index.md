---
title: Comment.AddReply
linktitle: AddReply
second_title: Aspose.Words for .NET API Reference
description: Comment AddReply method. Adds a reply to this comment in C#.
type: docs
weight: 120
url: /net/aspose.words/comment/addreply/
---
## AddReply method

Adds a reply to this comment.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | String | The author name for the reply. |
| initial | String | The author initials for the reply. |
| dateTime | DateTime | The date and time for the reply. |
| text | String | The reply text. |

### Return Value

The created [`Comment`](../) node for the reply.

## Remarks

Due to the existing MS Office limitations only 1 level of replies is allowed in the document. An exception of type InvalidOperationException will be raised if this method is called on the existing Reply comment.

## Examples

Shows how to add a comment to a document, and then reply to it.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Place the comment at a node in the document's body.
// This comment will show up at the location of its paragraph,
// outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder.CurrentParagraph.AppendChild(comment);

// Add a reply, which will show up under its parent comment.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Comments and replies are both Comment nodes.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Comments that do not reply to other comments are "top-level". They have no ancestor comments.
Assert.Null(comment.Ancestor);

// Replies have an ancestor top-level comment.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### See Also

* class [Comment](../)
* namespace [Aspose.Words](../../comment/)
* assembly [Aspose.Words](../../../)
