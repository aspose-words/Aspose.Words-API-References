---
title: Comment.Ancestor
second_title: Aspose.Words für .NET-API-Referenz
description: Comment eigendom. Gibt das übergeordnete Kommentarobjekt zurück. Gibt null für Kommentare der obersten Ebene zurück.
type: docs
weight: 20
url: /de/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Gibt das übergeordnete Kommentarobjekt zurück. Gibt null für Kommentare der obersten Ebene zurück.

```csharp
public Comment Ancestor { get; }
```

### Beispiele

Zeigt, wie alle Kommentare eines Dokuments und ihre Antworten gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// Wenn ein Kommentar keinen Vorfahren hat, handelt es sich um einen "Top-Level"-Kommentar im Gegensatz zu einem Antworttyp-Kommentar.
// Drucken Sie alle Kommentare der obersten Ebene zusammen mit allen möglichen Antworten.
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


