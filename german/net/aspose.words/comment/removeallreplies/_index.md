---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words für .NET
description: Comment RemoveAllReplies methode. Entfernt alle Antworten auf diesen Kommentar in C#.
type: docs
weight: 130
url: /de/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Entfernt alle Antworten auf diesen Kommentar.

```csharp
public void RemoveAllReplies()
```

## Bemerkungen

Alle Teilknoten der Antworten werden aus dem Dokument gelöscht.

## Beispiele

Zeigt, wie Kommentarantworten entfernt werden.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// Nachfolgend finden Sie zwei Möglichkeiten, Antworten aus einem Kommentar zu entfernen.
// 1 – Verwenden Sie die Methode „RemoveReply“, um Antworten einzeln aus einem Kommentar zu entfernen:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 – Verwenden Sie die Methode „RemoveAllReplies“, um alle Antworten aus einem Kommentar auf einmal zu entfernen:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### Siehe auch

* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
