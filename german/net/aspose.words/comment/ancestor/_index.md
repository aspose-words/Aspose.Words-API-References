---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words für .NET
description: Rufen Sie das übergeordnete Kommentarobjekt mit unserer Ancestor-Eigenschaft ab. Ideal für die Navigation in Kommentarthreads und die Steigerung der Benutzerinteraktion.
type: docs
weight: 20
url: /de/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Gibt das übergeordnete Element zurück[`Comment`](../)Objekt. Gibt zurück`null` für Kommentare der obersten Ebene.

```csharp
public Comment Ancestor { get; }
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

* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
