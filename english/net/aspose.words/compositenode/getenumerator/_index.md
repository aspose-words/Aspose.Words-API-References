---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: Explore the CompositeNode GetEnumerator method for seamless iteration over child nodes. Enhance your coding efficiency with this powerful feature!
type: docs
weight: 120
url: /net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Provides support for the for each style iteration over the child nodes of this node.

```csharp
public IEnumerator<Node> GetEnumerator()
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

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
