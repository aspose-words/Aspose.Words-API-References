---
title: Inline.IsMoveFromRevision
second_title: Aspose.Words für .NET-API-Referenz
description: Inline eigendom. Gibt zurückWAHR wenn dieses Objekt in Microsoft Word verschoben gelöscht wurde während die Änderungsverfolgung aktiviert war.
type: docs
weight: 50
url: /de/net/aspose.words/inline/ismovefromrevision/
---
## Inline.IsMoveFromRevision property

Gibt zurück`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsMoveFromRevision { get; }
```

### Beispiele

Zeigt, wie der Revisionstyp eines Inline-Knotens ermittelt wird.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Wenn wir das Dokument bearbeiten, während die Option „Änderungen verfolgen“ über „Überprüfen ->“ verfügbar ist. Verfolgung,
// in Microsoft Word aktiviert ist, gelten die von uns vorgenommenen Änderungen als Revisionen.
// Wenn wir ein Dokument mit Aspose.Words bearbeiten, können wir mit der Nachverfolgung von Revisionen beginnen
// Aufrufen der Methode „StartTrackRevisions“ des Dokuments und Stoppen der Verfolgung mithilfe der Methode „StopTrackRevisions“.
// Wir können entweder Revisionen akzeptieren, um sie in das Dokument zu integrieren
// oder lehnen Sie sie ab, um die vorgeschlagene Änderung wirksam zu ändern.
Assert.AreEqual(6, doc.Revisions.Count);

// Der übergeordnete Knoten einer Revision ist der Lauf, den die Revision betrifft. Ein Run ist ein Inline-Knoten.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Nachfolgend sind fünf Arten von Revisionen aufgeführt, die einen Inline-Knoten kennzeichnen können.
// 1 – Eine „einfügen“-Revision:
// Diese Überarbeitung erfolgt, wenn wir Text einfügen und gleichzeitig Änderungen verfolgen.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 – Eine „Format“-Revision:
// Diese Überarbeitung erfolgt, wenn wir die Textformatierung ändern und gleichzeitig Änderungen verfolgen.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 – Eine „Move from“-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// Beim Verfolgen von Änderungen werden zwei Revisionen angezeigt.
// Die „Verschieben von“-Revision ist eine Kopie des ursprünglichen Textes, bevor wir ihn verschoben haben.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 – Eine „Move to“-Revision:
// Die „Verschieben nach“-Revision ist der Text, den wir an seine neue Position im Dokument verschoben haben.
// „Verschieben von“- und „Verschieben nach“-Revisionen erscheinen paarweise für jede von uns durchgeführte Verschiebungsrevision.
// Durch das Akzeptieren einer Verschiebungsrevision werden die „Verschiebung von“-Revision und ihr Text gelöscht.
// und behält den Text aus der „Verschieben nach“-Revision.
// Wenn Sie eine Verschiebungsrevision ablehnen, bleibt umgekehrt die „Verschieben von“-Revision erhalten und die „Verschieben nach“-Revision wird gelöscht.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 – Eine „Lösch“-Revision:
// Diese Überarbeitung erfolgt, wenn wir Text löschen, während wir Änderungen verfolgen. Wenn wir Text wie diesen löschen,
// es bleibt als Revision im Dokument, bis wir entweder die Revision akzeptieren,
// wodurch der Text endgültig gelöscht wird oder die Überarbeitung abgelehnt wird, wodurch der von uns gelöschte Text dort verbleibt, wo er war.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Siehe auch

* class [Inline](../)
* namensraum [Aspose.Words](../../inline/)
* Montage [Aspose.Words](../../../)


