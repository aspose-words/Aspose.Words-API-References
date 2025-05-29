---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words för .NET
description: Upptäck kommentarsvar. Få tillgång till en samling kommentarobjekt som är direkta svar på din angivna kommentar, vilket förbättrar användarengagemang och interaktion.
type: docs
weight: 110
url: /sv/net/aspose.words/comment/replies/
---
## Comment.Replies property

Returnerar en samling av[`Comment`](../) objekt som är omedelbara underordnade till den angivna kommentaren.

```csharp
public CommentCollection Replies { get; }
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

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
