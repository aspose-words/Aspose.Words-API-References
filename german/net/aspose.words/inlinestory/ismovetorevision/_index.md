---
title: InlineStory.IsMoveToRevision
second_title: Aspose.Words für .NET-API-Referenz
description: InlineStory eigendom. Gibt zurückWAHR wenn dieses Objekt in Microsoft Word verschoben eingefügt wurde während die Änderungsverfolgung aktiviert war.
type: docs
weight: 60
url: /de/net/aspose.words/inlinestory/ismovetorevision/
---
## InlineStory.IsMoveToRevision property

Gibt zurück`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsMoveToRevision { get; }
```

### Beispiele

Zeigt, wie revisionsbezogene Eigenschaften von InlineStory-Knoten angezeigt werden.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Wenn wir das Dokument bearbeiten, während die Option „Änderungen verfolgen“ über „Überprüfen ->“ verfügbar ist. Verfolgung,
// in Microsoft Word aktiviert ist, gelten die von uns vorgenommenen Änderungen als Revisionen.
// Wenn wir ein Dokument mit Aspose.Words bearbeiten, können wir mit der Nachverfolgung von Revisionen beginnen
// Aufrufen der Methode „StartTrackRevisions“ des Dokuments und Stoppen der Verfolgung mithilfe der Methode „StopTrackRevisions“.
// Wir können entweder Revisionen akzeptieren, um sie in das Dokument zu integrieren
// oder lehnen Sie sie ab, um die vorgeschlagene Änderung rückgängig zu machen und zu verwerfen.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Nachfolgend sind fünf Arten von Revisionen aufgeführt, die einen InlineStory-Knoten kennzeichnen können.
// 1 – Eine „einfügen“-Revision:
// Diese Überarbeitung erfolgt, wenn wir Text einfügen und gleichzeitig Änderungen verfolgen.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 – Eine „Move from“-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// Beim Verfolgen von Änderungen werden zwei Revisionen angezeigt.
// Die „Verschieben von“-Revision ist eine Kopie des ursprünglichen Textes, bevor wir ihn verschoben haben.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 – Eine „Move to“-Revision:
// Die „Verschieben nach“-Revision ist der Text, den wir an seine neue Position im Dokument verschoben haben.
// „Verschieben von“- und „Verschieben nach“-Revisionen erscheinen paarweise für jede von uns durchgeführte Verschiebungsrevision.
// Durch das Akzeptieren einer Verschiebungsrevision werden die „Verschiebung von“-Revision und ihr Text gelöscht.
// und behält den Text aus der „Verschieben nach“-Revision.
// Wenn Sie eine Verschiebungsrevision ablehnen, bleibt umgekehrt die „Verschieben von“-Revision erhalten und die „Verschieben nach“-Revision wird gelöscht.
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 – Eine „Lösch“-Revision:
// Diese Überarbeitung erfolgt, wenn wir Text löschen, während wir Änderungen verfolgen. Wenn wir Text wie diesen löschen,
// es bleibt als Revision im Dokument, bis wir entweder die Revision akzeptieren,
// wodurch der Text endgültig gelöscht wird oder die Überarbeitung abgelehnt wird, wodurch der von uns gelöschte Text dort verbleibt, wo er war.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Siehe auch

* class [InlineStory](../)
* namensraum [Aspose.Words](../../inlinestory/)
* Montage [Aspose.Words](../../../)


