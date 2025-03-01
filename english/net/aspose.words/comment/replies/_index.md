---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words for .NET
description: Discover Comment Replies. Access a collection of Comment objects that are direct responses to your specified comment, enhancing user engagement and interaction.
type: docs
weight: 110
url: /net/aspose.words/comment/replies/
---
## Comment.Replies property

Returns a collection of [`Comment`](../) objects that are immediate children of the specified comment.

```csharp
public CommentCollection Replies { get; }
```

## Examples

Shows how to print all of a document's comments and their replies.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
// Print all top-level comments along with any replies they may have.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

### See Also

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
