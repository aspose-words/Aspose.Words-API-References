---
title: Class ParagraphCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.ParagraphCollection klas. Bietet typisierten Zugriff auf eine Sammlung vonParagraph Knoten.
type: docs
weight: 4410
url: /de/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Bietet typisierten Zugriff auf eine Sammlung von[`Paragraph`](../paragraph/) Knoten.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Absätzen](https://docs.aspose.com/words/net/working-with-paragraphs/) Dokumentationsartikel.

```csharp
public class ParagraphCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Ruft a ab[`Paragraph`](../paragraph/) am angegebenen Index. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Sammlung von Knoten. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Fügt am angegebenen Index einen Knoten in die Sammlung ein. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Kopiert alle Absätze aus der Sammlung in ein neues Array von Absätzen. (2 methods) |

### Beispiele

Zeigt, wie überprüft wird, ob es sich bei einem Absatz um eine Verschiebungsrevision handelt.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Dieses Dokument enthält „Verschieben“-Revisionen, die angezeigt werden, wenn wir Text mit dem Cursor markieren.
// und ziehen Sie es dann, um es an eine andere Position zu verschieben
// während Überarbeitungen in Microsoft Word über „Überprüfen“ verfolgt werden -> "Änderungen verfolgen".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Verschieberevisionen bestehen aus Paaren von „Verschieben von“- und „Verschieben nach“-Revisionen.
// Bei diesen Überarbeitungen handelt es sich um potenzielle Änderungen am Dokument, die wir entweder akzeptieren oder ablehnen können.
// Bevor wir eine Verschiebungsrevision akzeptieren/ablehnen, das Dokument
// muss sowohl das Abflug- als auch das Ankunftsziel des Textes im Auge behalten.
// Der zweite und der vierte Absatz definieren eine solche Revision und haben daher beide den gleichen Inhalt.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Die Revision „Verschieben von“ ist der Absatz, aus dem wir den Text gezogen haben.
// Wenn wir die Überarbeitung akzeptieren, wird dieser Absatz verschwinden,
// und der andere bleibt bestehen und ist keine Revision mehr.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Die „Verschieben nach“-Revision ist der Absatz, in den wir den Text gezogen haben.
// Wenn wir die Überarbeitung ablehnen, verschwindet stattdessen dieser Absatz und der andere bleibt bestehen.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Siehe auch

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


