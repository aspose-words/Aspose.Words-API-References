---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words für .NET
description: Comment AddReply methode. Fügt eine Antwort zu diesem Kommentar hinzu in C#.
type: docs
weight: 120
url: /de/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Fügt eine Antwort zu diesem Kommentar hinzu.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| author | String | Der Name des Autors für die Antwort. |
| initial | String | Die Initialen des Autors für die Antwort. |
| dateTime | DateTime | Datum und Uhrzeit der Antwort. |
| text | String | Der Antworttext. |

### Rückgabewert

Das Geschaffene[`Comment`](../) Knoten für die Antwort.

## Bemerkungen

Aufgrund der bestehenden MS Office-Einschränkungen ist im Dokument nur eine Ebene von Antworten zulässig. Eine Ausnahme dieser ArtInvalidOperationException wird ausgelöst, wenn diese Methode für den vorhandenen Antwortkommentar aufgerufen wird.

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
