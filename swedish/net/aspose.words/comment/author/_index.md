---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words för .NET
description: Hantera kommentarförfattare enkelt med egenskapen Kommentarförfattare. Returnera eller ange enkelt författarnamn för att förbättra användarengagemang och innehållets tydlighet.
type: docs
weight: 30
url: /sv/net/aspose.words/comment/author/
---
## Comment.Author property

Returnerar eller anger författarnamnet för en kommentar.

```csharp
public string Author { get; set; }
```

## Anmärkningar

Kan inte vara`null`.

Standardvärdet är en tom sträng.

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
