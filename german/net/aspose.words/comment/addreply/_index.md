---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Diskussionen mit der Methode „Comment AddReply“ – fügen Sie Kommentaren ganz einfach Antworten hinzu und verbessern Sie das Engagement auf Ihrer Plattform!
type: docs
weight: 160
url: /de/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Fügt eine Antwort auf diesen Kommentar hinzu.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| author | String | Der Name des Autors der Antwort. |
| initial | String | Die Initialen des Autors für die Antwort. |
| dateTime | DateTime | Datum und Uhrzeit der Antwort. |
| text | String | Der Antworttext. |

### Rückgabewert

Die geschaffene[`Comment`](../) Knoten für die Antwort.

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| InvalidOperationException | Wird ausgelöst, wenn diese Methode für den vorhandenen Antwortkommentar aufgerufen wird. |

## Bemerkungen

Aufgrund der bestehenden MS Office-Einschränkungen ist im Dokument nur eine Antwortebene zulässig.

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
