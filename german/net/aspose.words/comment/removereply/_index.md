---
title: Comment.RemoveReply
linktitle: RemoveReply
articleTitle: RemoveReply
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos unerwünschte Antworten mit der Methode „Comment RemoveReply“ und sorgen Sie so dafür, dass Ihre Diskussionen klar und relevant bleiben. Verbessern Sie noch heute Ihr Kommentarmanagement!
type: docs
weight: 180
url: /de/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

Entfernt die angegebene Antwort auf diesen Kommentar.

```csharp
public void RemoveReply(Comment reply)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| reply | Comment | Der Kommentarknoten der Löschantwort. |

## Bemerkungen

Alle Bestandteile der Antwort werden aus dem Dokument gelöscht.

## Beispiele

Zeigt, wie Kommentarantworten entfernt werden.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// Unten finden Sie zwei Möglichkeiten zum Entfernen von Antworten aus einem Kommentar.
// 1 - Verwenden Sie die Methode „RemoveReply“, um Antworten aus einem Kommentar einzeln zu entfernen:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 – Verwenden Sie die Methode „RemoveAllReplies“, um alle Antworten eines Kommentars auf einmal zu entfernen:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Siehe auch

* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
