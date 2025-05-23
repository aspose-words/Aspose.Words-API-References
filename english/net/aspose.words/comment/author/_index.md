---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words for .NET
description: Manage comment authors effortlessly with the Comment Author property. Easily return or set author names to enhance user engagement and content clarity.
type: docs
weight: 30
url: /net/aspose.words/comment/author/
---
## Comment.Author property

Returns or sets the author name for a comment.

```csharp
public string Author { get; set; }
```

## Remarks

Cannot be `null`.

Default is empty string.

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

* class [Comment](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
