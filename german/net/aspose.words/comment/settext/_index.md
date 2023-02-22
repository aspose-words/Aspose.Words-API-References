---
title: Comment.SetText
second_title: Aspose.Words für .NET-API-Referenz
description: Comment methode. Dies ist eine bequeme Methode mit der Sie den Text des Kommentars einfach festlegen können.
type: docs
weight: 150
url: /de/net/aspose.words/comment/settext/
---
## Comment.SetText method

Dies ist eine bequeme Methode, mit der Sie den Text des Kommentars einfach festlegen können.

```csharp
public void SetText(string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| text | String | Der neue Text des Kommentars. |

### Bemerkungen

Diese Methode ermöglicht es, den Text eines Kommentars schnell aus einer Zeichenfolge festzulegen. Der String kann Absatzumbrüche enthalten, dadurch werden im Kommentar entsprechende Textabsätze erzeugt. Wenn Sie komplexere Elemente in den Kommentar einfügen wollen, zB Lesezeichen oder Tabellen oder Rich Formatting anwenden, müssen Sie die entsprechenden Node-Klassen verwenden bis den Kommentartext aufbauen.

### Beispiele

Zeigt, wie Sie einem Dokument einen Kommentar hinzufügen und darauf antworten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Platziere den Kommentar an einem Knoten im Hauptteil des Dokuments.
// Dieser Kommentar wird an der Stelle seines Absatzes angezeigt,
// außerhalb des rechten Rands der Seite und mit einer gepunkteten Linie, die ihn mit seinem Absatz verbindet.
builder.CurrentParagraph.AppendChild(comment);

// Füge eine Antwort hinzu, die unter dem übergeordneten Kommentar angezeigt wird.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Kommentare und Antworten sind beide Kommentarknoten.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Kommentare, die nicht auf andere Kommentare antworten, sind "oberste Ebene". Sie haben keine Vorfahrenkommentare.
Assert.Null(comment.Ancestor);

// Antworten haben einen übergeordneten Kommentar auf oberster Ebene.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Siehe auch

* class [Comment](../)
* namensraum [Aspose.Words](../../comment/)
* Montage [Aspose.Words](../../../)


