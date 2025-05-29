---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words für .NET
description: Verwalten Sie Kommentarautoren mühelos mit der Eigenschaft „Kommentarautor“. Geben Sie Autorennamen einfach zurück oder legen Sie sie fest, um die Benutzerinteraktion und die Inhaltsübersicht zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words/comment/author/
---
## Comment.Author property

Gibt den Autorennamen für einen Kommentar zurück oder legt ihn fest.

```csharp
public string Author { get; set; }
```

## Bemerkungen

Kann nicht sein`null`.

Der Standardwert ist eine leere Zeichenfolge.

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
