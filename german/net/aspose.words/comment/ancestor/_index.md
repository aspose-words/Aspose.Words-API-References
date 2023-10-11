---
title: Comment.Ancestor
second_title: Aspose.Words für .NET-API-Referenz
description: Comment eigendom. Gibt das übergeordnete Element zurückComment Objekt. Kehrt zurückNull für Kommentare der obersten Ebene.
type: docs
weight: 20
url: /de/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Gibt das übergeordnete Element zurück[`Comment`](../) Objekt. Kehrt zurück`Null` für Kommentare der obersten Ebene.

```csharp
public Comment Ancestor { get; }
```

### Beispiele

Zeigt, wie alle Kommentare und Antworten eines Dokuments gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Wenn ein Kommentar keinen Vorfahren hat, handelt es sich um einen „Top-Level“-Kommentar und nicht um einen Antworttyp-Kommentar.
// Alle Kommentare der obersten Ebene zusammen mit etwaigen Antworten drucken.
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

### Siehe auch

* class [Comment](../)
* namensraum [Aspose.Words](../../comment/)
* Montage [Aspose.Words](../../../)


