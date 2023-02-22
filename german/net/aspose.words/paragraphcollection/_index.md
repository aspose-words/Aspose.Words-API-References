---
title: Class ParagraphCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.ParagraphCollection klas. Bietet getippten Zugriff auf eine Sammlung vonParagraph Knoten.
type: docs
weight: 4170
url: /de/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Bietet getippten Zugriff auf eine Sammlung von[`Paragraph`](../paragraph/) Knoten.

```csharp
public class ParagraphCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Ruft a **Absatz** am angegebenen Index. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Fügt am Ende der Sammlung einen Knoten hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Bestimmt, ob sich ein Knoten in der Sammlung befindet. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im "foreach"-Stil über die Sammlung von Knoten. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Fügt am angegebenen Index einen Knoten in die Sammlung ein. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Kopiert alle Absätze aus der Sammlung in ein neues Array von Absätzen. (2 methods) |

### Beispiele

Zeigt, wie überprüft wird, ob es sich bei einem Absatz um eine verschobene Überarbeitung handelt.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Dieses Dokument enthält "Move"-Revisionen, die erscheinen, wenn wir Text mit dem Cursor markieren,
// und ziehen Sie es dann, um es an eine andere Position zu verschieben
// beim Verfolgen von Revisionen in Microsoft Word über "Review" -> "Änderungen verfolgen".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Verschiebungsrevisionen bestehen aus Paaren von "Move from"- und "Move to"-Revisionen. 
// Diese Überarbeitungen sind potenzielle Änderungen am Dokument, die wir entweder akzeptieren oder ablehnen können.
// Bevor wir eine Move-Revision akzeptieren/ablehnen, wird das Dokument
// muss sowohl die Abfahrts- als auch die Ankunftsziele des Textes verfolgen.
// Der zweite und der vierte Absatz definieren eine solche Überarbeitung und haben daher beide den gleichen Inhalt.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Die „Move from“-Revision ist der Absatz, aus dem wir den Text gezogen haben.
// Wenn wir die Überarbeitung akzeptieren, verschwindet dieser Absatz,
// und der andere bleibt bestehen und ist keine Revision mehr.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Die Revision „Verschieben nach“ ist der Absatz, in den wir den Text gezogen haben.
// Wenn wir die Überarbeitung ablehnen, verschwindet stattdessen dieser Absatz und der andere bleibt bestehen.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Siehe auch

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


