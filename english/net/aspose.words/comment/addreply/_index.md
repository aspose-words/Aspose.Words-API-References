---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words for .NET
description: Enhance your discussions with the Comment AddReply method—easily add replies to comments and improve engagement on your platform!
type: docs
weight: 160
url: /net/aspose.words/comment/addreply/
---
## Comment.AddReply method

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

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Throws if this method is called on the existing Reply comment. |

## Remarks

Due to the existing MS Office limitations only 1 level of replies is allowed in the document.

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
Assert.That(doc.GetChildNodes(NodeType.Comment, true).Count, Is.EqualTo(2));

// Comments that do not reply to other comments are "top-level". They have no ancestor comments.
Assert.That(comment.Ancestor, Is.Null);

// Replies have an ancestor top-level comment.
Assert.That(comment.Replies[0].Ancestor, Is.EqualTo(comment));

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### See Also

* class [Comment](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
