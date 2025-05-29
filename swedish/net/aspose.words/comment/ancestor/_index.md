---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words för .NET
description: Hämta det överordnade kommentarobjektet med vår Ancestor-egenskap. Perfekt för att navigera i kommentarstrådar och förbättra användarengagemang.
type: docs
weight: 20
url: /sv/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Returnerar föräldern[`Comment`](../)objekt. Returnerar`null` för kommentarer på toppnivå.

```csharp
public Comment Ancestor { get; }
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

* class [Comment](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
