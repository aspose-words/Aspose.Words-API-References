---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words for .NET
description: Discover the SetText method, a user-friendly tool that simplifies adding comments, enhancing your workflow and boosting productivity effortlessly.
type: docs
weight: 190
url: /net/aspose.words/comment/settext/
---
## Comment.SetText method

This is a convenience method that allows to easily set text of the comment.

```csharp
public void SetText(string text)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | String | The new text of the comment. |

## Remarks

This method allows to quickly set text of a comment from a string. The string can contain paragraph breaks, this will create paragraphs of text in the comment accordingly. If you want to insert more complex elements into the comment, for example bookmarks or tables or apply rich formatting, then you need to use the appropriate node classes to build up the comment text.

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
