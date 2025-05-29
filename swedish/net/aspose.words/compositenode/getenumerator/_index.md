---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: Utforska metoden CompositeNode GetEnumerator för sömlös iteration över underordnade noder. Förbättra din kodningseffektivitet med den här kraftfulla funktionen!
type: docs
weight: 120
url: /sv/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod.

```csharp
public IEnumerator<Node> GetEnumerator()
```

## Exempel

Visar hur man skriver ut alla kommentarer och svar i ett dokument.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Om en kommentar inte har någon överordnad kommentar är det en kommentar på "toppnivå" i motsats till en kommentar av svarstyp.
// Skriv ut alla kommentarer på toppnivå tillsammans med eventuella svar.
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

### Se även

* class [Node](../../node/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
