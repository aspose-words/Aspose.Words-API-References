---
title: RunCollection Class
linktitle: RunCollection
articleTitle: RunCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.RunCollection für nahtlosen Zugriff auf Run-Knoten. Verbessern Sie Ihre Dokumentverarbeitung mit leistungsstarken, typisierten Funktionen!
type: docs
weight: 5570
url: /de/net/aspose.words/runcollection/
---
## RunCollection class

Bietet typisierten Zugriff auf eine Sammlung von[`Run`](../run/) Knoten.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class RunCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/runcollection/item/) { get; } | Ruft eine[`Run`](../run/) am angegebenen Index. (2 indexers) |

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
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Kopiert alle Läufe aus der Sammlung in ein neues Array von Läufen. (2 methods) |

## Beispiele

Zeigt, wie der Revisionstyp eines Inline-Knotens bestimmt wird.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Wenn wir das Dokument bearbeiten, während die Option "Änderungen verfolgen" aktiviert ist, die Sie über Überprüfen -> Verfolgung finden,
// in Microsoft Word aktiviert ist, zählen die von uns vorgenommenen Änderungen als Revisionen.
// Wenn wir ein Dokument mit Aspose.Words bearbeiten, können wir mit der Verfolgung von Revisionen beginnen, indem wir
// Aufrufen der Methode „StartTrackRevisions“ des Dokuments und Beenden der Verfolgung mithilfe der Methode „StopTrackRevisions“.
// Wir können entweder Revisionen akzeptieren, um sie in das Dokument zu integrieren
// oder lehnen Sie sie ab, um die vorgeschlagene Änderung wirksam umzusetzen.
Assert.AreEqual(6, doc.Revisions.Count);

// Der übergeordnete Knoten einer Revision ist der Lauf, auf den sich die Revision bezieht. Ein Lauf ist ein Inline-Knoten.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Unten sind fünf Revisionstypen aufgeführt, die einen Inline-Knoten kennzeichnen können.
// 1 - Eine "Insert"-Revision:
// Diese Überarbeitung erfolgt, wenn wir beim Verfolgen von Änderungen Text einfügen.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Eine „Format“-Revision:
// Diese Überarbeitung erfolgt, wenn wir die Formatierung des Textes ändern, während wir Änderungen verfolgen.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Eine „Move from“-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// Beim Verfolgen von Änderungen werden zwei Revisionen angezeigt.
// Die „Verschieben von“-Revision ist eine Kopie des ursprünglichen Textes, bevor wir ihn verschoben haben.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Eine „Verschieben nach“-Revision:
// Die „Verschieben nach“-Revision ist der Text, den wir an seine neue Position im Dokument verschoben haben.
// Die Revisionen „Verschieben von“ und „Verschieben nach“ werden bei jeder von uns durchgeführten Verschiebungsrevision paarweise angezeigt.
// Das Akzeptieren einer Verschiebungsrevision löscht die „Verschieben von“-Revision und ihren Text,
// und behält den Text aus der „Verschieben nach“-Revision bei.
// Das Ablehnen einer Verschiebungsrevision behält umgekehrt die „Verschieben von“-Revision bei und löscht die „Verschieben nach“-Revision.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Eine „Löschen“-Revision:
// Diese Überarbeitung erfolgt, wenn wir Text löschen, während wir Änderungen verfolgen. Wenn wir Text wie diesen löschen,
// es bleibt als Revision im Dokument, bis wir die Revision entweder akzeptieren,
// wodurch der Text endgültig gelöscht wird, oder die Überarbeitung abgelehnt wird, wodurch der gelöschte Text dort bleibt, wo er war.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Siehe auch

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
