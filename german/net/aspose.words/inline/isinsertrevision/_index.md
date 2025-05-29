---
title: Inline.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words für .NET
description: Entdecken Sie die Inline-Eigenschaft IsInsertRevision. Überprüfen Sie einfach, ob ein Objekt in Word mit aktivierter Änderungsverfolgung hinzugefügt wurde. Optimieren Sie Ihr Dokumentenmanagement!
type: docs
weight: 40
url: /de/net/aspose.words/inline/isinsertrevision/
---
## Inline.IsInsertRevision property

Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsInsertRevision { get; }
```

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

* class [Inline](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
