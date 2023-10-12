---
title: Comment.Author
second_title: Aspose.Words för .NET API Referens
description: Comment fast egendom. Returnerar eller ställer in författarens namn för en kommentar.
type: docs
weight: 30
url: /sv/net/aspose.words/comment/author/
---
## Comment.Author property

Returnerar eller ställer in författarens namn för en kommentar.

```csharp
public string Author { get; set; }
```

### Anmärkningar

Kan inte vara`null`.

Standard är tom sträng.

### Exempel

Visar hur du skriver ut alla kommentarer i ett dokument och deras svar.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Om en kommentar inte har någon förfader är den en kommentar på "toppnivå" i motsats till en kommentar av typen svar.
// Skriv ut alla kommentarer på toppnivå tillsammans med eventuella svar de kan ha.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
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
* namnutrymme [Aspose.Words](../../comment/)
* hopsättning [Aspose.Words](../../../)


