---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mit der CommentCollection-Elementeigenschaft mühelos auf bestimmte Kommentare zu. Rufen Sie Kommentare nach Index ab, um die Inhaltsverwaltung zu optimieren.
type: docs
weight: 10
url: /de/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Ruft eine[`Comment`](../../comment/) am angegebenen Index.

```csharp
public Comment this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index zur Sammlung. |

## Bemerkungen

Der Index ist nullbasiert.

Negative Indizes sind zulässig und zeigen den Zugriff vom Ende der Sammlung an. Beispielsweise bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

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

* class [Comment](../../comment/)
* class [CommentCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
