---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words für .NET
description: Entdecken Sie die SetText-Methode, ein benutzerfreundliches Tool, das das Hinzufügen von Kommentaren vereinfacht, Ihren Arbeitsablauf verbessert und die Produktivität mühelos steigert.
type: docs
weight: 190
url: /de/net/aspose.words/comment/settext/
---
## Comment.SetText method

Dies ist eine praktische Methode, mit der sich der Kommentartext einfach festlegen lässt.

```csharp
public void SetText(string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| text | String | Der neue Text des Kommentars. |

## Bemerkungen

Mit dieser Methode lässt sich der Text eines Kommentars schnell aus einer Zeichenfolge erstellen. Die Zeichenfolge kann Absatzumbrüche enthalten, wodurch im Kommentar entsprechende Textabsätze erstellt werden. Wenn Sie komplexere Elemente in den Kommentar einfügen möchten, z. B. Lesezeichen, Tabellen oder eine umfangreiche Formatierung, müssen Sie die entsprechenden Knotenklassen verwenden, um den Kommentartext zu erstellen.

## Beispiele

Zeigt, wie Sie einem Dokument einen Kommentar hinzufügen und dann darauf antworten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Platzieren Sie den Kommentar an einem Knoten im Hauptteil des Dokuments.
// Dieser Kommentar wird an der Stelle seines Absatzes angezeigt,
// außerhalb des rechten Seitenrands und mit einer gepunkteten Linie, die es mit dem Absatz verbindet.
builder.CurrentParagraph.AppendChild(comment);

// Fügen Sie eine Antwort hinzu, die unter dem übergeordneten Kommentar angezeigt wird.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Kommentare und Antworten sind beides Kommentarknoten.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Kommentare, die nicht auf andere Kommentare antworten, sind „Top-Level“. Sie haben keine übergeordneten Kommentare.
Assert.Null(comment.Ancestor);

// Antworten haben einen übergeordneten Kommentar auf oberster Ebene.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Siehe auch

* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
