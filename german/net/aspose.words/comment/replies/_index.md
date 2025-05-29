---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words für .NET
description: Entdecken Sie Kommentarantworten. Greifen Sie auf eine Sammlung von Kommentarobjekten zu, die direkte Antworten auf Ihren angegebenen Kommentar sind und so die Benutzerinteraktion und -einbindung verbessern.
type: docs
weight: 110
url: /de/net/aspose.words/comment/replies/
---
## Comment.Replies property

Gibt eine Sammlung von[`Comment`](../) Objekte, die unmittelbare untergeordnete Objekte des angegebenen Kommentars sind.

```csharp
public CommentCollection Replies { get; }
```

## Beispiele

Zeigt, wie alle Kommentare und Antworten eines Dokuments gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Wenn ein Kommentar keinen Vorgänger hat, handelt es sich um einen Kommentar der obersten Ebene und nicht um einen Kommentar vom Typ „Antwort“.
// Alle Kommentare der obersten Ebene zusammen mit allen möglichen Antworten ausdrucken.
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

### Siehe auch

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
