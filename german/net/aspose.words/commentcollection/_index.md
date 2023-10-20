---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.CommentCollection klas. Bietet typisierten Zugriff auf eine Sammlung vonComment Knoten in C#.
type: docs
weight: 240
url: /de/net/aspose.words/commentcollection/
---
## CommentCollection class

Bietet typisierten Zugriff auf eine Sammlung von[`Comment`](../comment/) Knoten.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Kommentaren](https://docs.aspose.com/words/net/working-with-comments/) Dokumentationsartikel.

```csharp
public class CommentCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Ruft a ab[`Comment`](../comment/) am angegebenen Index. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Sammlung von Knoten. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Fügt am angegebenen Index einen Knoten in die Sammlung ein. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Kopiert alle Knoten aus der Sammlung in ein neues Array von Knoten. |

## Beispiele

Zeigt, wie man einen Kommentar als „erledigt“ markiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Einen Kommentar einfügen, um auf einen Fehler hinzuweisen.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // Kommentare haben ein „Fertig“-Flag, das standardmäßig auf „false“ gesetzt ist.
// Wenn ein Kommentar darauf hindeutet, dass wir eine Änderung im Dokument vornehmen,
// Wir können die Änderung übernehmen und anschließend auch das Flag „Fertig“ setzen, um die Korrektur anzuzeigen.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Kommentare, die „erledigt“ sind, differenzieren sich
// von denen, die mit einer verblassten Textfarbe noch nicht „fertig“ sind.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Siehe auch

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
