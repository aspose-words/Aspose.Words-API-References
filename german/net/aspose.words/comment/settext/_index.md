---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words für .NET
description: Comment SetText methode. Dies ist eine praktische Methode die es ermöglicht den Text des Kommentars einfach festzulegen in C#.
type: docs
weight: 150
url: /de/net/aspose.words/comment/settext/
---
## Comment.SetText method

Dies ist eine praktische Methode, die es ermöglicht, den Text des Kommentars einfach festzulegen.

```csharp
public void SetText(string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| text | String | Der neue Text des Kommentars. |

## Bemerkungen

Mit dieser Methode können Sie schnell den Text eines Kommentars aus einer Zeichenfolge festlegen. Der String kann Absatzumbrüche enthalten, dadurch werden entsprechend Textabsätze im Kommentar erstellt. Wenn Sie komplexere Elemente in den Kommentar einfügen möchten, zum Beispiel Lesezeichen oder Tabellen oder Rich-Formatierung anwenden möchten, müssen Sie die entsprechenden Knotenklassen verwenden um den Kommentartext aufzubauen.

## Beispiele

Zeigt, wie man einem Dokument einen Kommentar hinzufügt und dann darauf antwortet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Platzieren Sie den Kommentar an einem Knoten im Hauptteil des Dokuments.
// Dieser Kommentar wird an der Stelle seines Absatzes angezeigt.
// außerhalb des rechten Randes der Seite und mit einer gepunkteten Linie, die es mit seinem Absatz verbindet.
builder.CurrentParagraph.AppendChild(comment);

// Eine Antwort hinzufügen, die unter dem übergeordneten Kommentar angezeigt wird.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Kommentare und Antworten sind beide Kommentarknoten.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Kommentare, die nicht auf andere Kommentare antworten, sind „Top-Level“. Sie haben keine Vorfahrenkommentare.
Assert.Null(comment.Ancestor);

// Antworten haben einen übergeordneten Kommentar auf oberster Ebene.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Siehe auch

* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
