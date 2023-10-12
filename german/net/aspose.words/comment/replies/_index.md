---
title: Comment.Replies
second_title: Aspose.Words für .NET-API-Referenz
description: Comment eigendom. Gibt eine Sammlung von zurückComment Objekte die unmittelbare untergeordnete Elemente des angegebenen Kommentars sind.
type: docs
weight: 100
url: /de/net/aspose.words/comment/replies/
---
## Comment.Replies property

Gibt eine Sammlung von zurück[`Comment`](../) Objekte, die unmittelbare untergeordnete Elemente des angegebenen Kommentars sind.

```csharp
public CommentCollection Replies { get; }
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

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* namensraum [Aspose.Words](../../comment/)
* Montage [Aspose.Words](../../../)


