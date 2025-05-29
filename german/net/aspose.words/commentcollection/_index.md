---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.CommentCollection für den einfachen Zugriff auf Kommentarknoten und verbessern Sie so die Dokumentbearbeitung und Zusammenarbeit in Ihren Projekten.
type: docs
weight: 430
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
| [Item](../../aspose.words/commentcollection/item/) { get; } | Ruft eine[`Comment`](../comment/) am angegebenen Index. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Fügt am Ende der Sammlung einen Knoten hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bestimmt, ob ein Knoten in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Knotensammlung. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Fügt einen Knoten am angegebenen Index in die Sammlung ein. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Kopiert alle Knoten aus der Sammlung in ein neues Knoten-Array. |

## Beispiele

Zeigt, wie ein Kommentar als „erledigt“ markiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

    // Fügen Sie einen Kommentar ein, um auf einen Fehler hinzuweisen.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

    // Kommentare haben ein „Erledigt“-Flag, das standardmäßig auf „false“ gesetzt ist.
// Wenn ein Kommentar vorschlägt, dass wir eine Änderung im Dokument vornehmen,
// wir können die Änderung anwenden und anschließend auch das Flag „Erledigt“ setzen, um die Korrektur anzuzeigen.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Kommentare, die "fertig" sind, werden sich unterscheiden
// von denen, die nicht „fertig“ sind, mit einer verblassten Textfarbe.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Siehe auch

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
