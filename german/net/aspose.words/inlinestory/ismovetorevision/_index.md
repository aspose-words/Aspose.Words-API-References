---
title: InlineStory.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsMoveToRevision-Eigenschaft von InlineStory und verfolgen Sie Änderungen in Microsoft Word ganz einfach mit dem Wahr/Falsch-Status für eine nahtlose Dokumentbearbeitung.
type: docs
weight: 60
url: /de/net/aspose.words/inlinestory/ismovetorevision/
---
## InlineStory.IsMoveToRevision property

Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsMoveToRevision { get; }
```

## Beispiele

Zeigt, wie revisionsbezogene Eigenschaften von InlineStory-Knoten angezeigt werden.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Wenn wir das Dokument bearbeiten, während die Option "Änderungen verfolgen" aktiviert ist, die Sie über Überprüfen -> Verfolgung finden,
// in Microsoft Word aktiviert ist, zählen die von uns vorgenommenen Änderungen als Revisionen.
// Wenn wir ein Dokument mit Aspose.Words bearbeiten, können wir mit der Verfolgung von Revisionen beginnen, indem wir
// Aufrufen der Methode „StartTrackRevisions“ des Dokuments und Beenden der Verfolgung mithilfe der Methode „StopTrackRevisions“.
// Wir können entweder Revisionen akzeptieren, um sie in das Dokument zu integrieren
// oder lehnen Sie sie ab, um die vorgeschlagene Änderung rückgängig zu machen und zu verwerfen.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Unten sind fünf Revisionstypen aufgeführt, die einen InlineStory-Knoten kennzeichnen können.
// 1 - Eine "Insert"-Revision:
// Diese Überarbeitung erfolgt, wenn wir beim Verfolgen von Änderungen Text einfügen.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Eine „Move from“-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// Beim Verfolgen von Änderungen werden zwei Revisionen angezeigt.
// Die „Verschieben von“-Revision ist eine Kopie des ursprünglichen Textes, bevor wir ihn verschoben haben.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Eine „Verschieben nach“-Revision:
// Die „Verschieben nach“-Revision ist der Text, den wir an seine neue Position im Dokument verschoben haben.
// Die Revisionen „Verschieben von“ und „Verschieben nach“ werden bei jeder von uns durchgeführten Verschiebungsrevision paarweise angezeigt.
// Das Akzeptieren einer Verschiebungsrevision löscht die „Verschieben von“-Revision und ihren Text,
// und behält den Text aus der „Verschieben nach“-Revision bei.
// Das Ablehnen einer Verschiebungsrevision behält umgekehrt die „Verschieben von“-Revision bei und löscht die „Verschieben nach“-Revision.
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Eine „Löschen“-Revision:
// Diese Überarbeitung erfolgt, wenn wir Text löschen, während wir Änderungen verfolgen. Wenn wir Text wie diesen löschen,
// es bleibt als Revision im Dokument, bis wir die Revision entweder akzeptieren,
// wodurch der Text endgültig gelöscht wird, oder die Überarbeitung abgelehnt wird, wodurch der gelöschte Text dort bleibt, wo er war.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Siehe auch

* class [InlineStory](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
