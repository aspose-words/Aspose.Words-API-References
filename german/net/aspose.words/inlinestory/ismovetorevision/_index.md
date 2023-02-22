---
title: InlineStory.IsMoveToRevision
second_title: Aspose.Words für .NET-API-Referenz
description: InlineStory eigendom. gibt zurück Stimmt wenn dieses Objekt in Microsoft Word verschoben eingefügt wurde während die Änderungsnachverfolgung aktiviert war.
type: docs
weight: 60
url: /de/net/aspose.words/inlinestory/ismovetorevision/
---
## InlineStory.IsMoveToRevision property

gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war.

```csharp
public bool IsMoveToRevision { get; }
```

### Beispiele

Zeigt, wie revisionsbezogene Eigenschaften von InlineStory-Knoten angezeigt werden.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Wenn wir das Dokument bearbeiten, während die Option „Änderungen nachverfolgen“ unter „Überprüfen“ -> Verfolgung,
// in Microsoft Word aktiviert ist, zählen die von uns vorgenommenen Änderungen als Überarbeitungen.
// Wenn wir ein Dokument mit Aspose.Words bearbeiten, können wir mit der Nachverfolgung von Revisionen beginnen
// die Methode „StartTrackRevisions“ des Dokuments aufrufen und die Nachverfolgung mit der Methode „StopTrackRevisions“ beenden.
// Wir können entweder Überarbeitungen akzeptieren, um sie in das Dokument zu integrieren
// oder sie ablehnen, um die vorgeschlagene Änderung rückgängig zu machen und zu verwerfen.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Nachfolgend sind fünf Arten von Revisionen aufgeführt, die einen InlineStory-Knoten kennzeichnen können.
// 1 - Eine "insert"-Revision:
// Diese Überarbeitung tritt auf, wenn wir Text einfügen, während wir Änderungen verfolgen.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Eine "Move from"-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// Beim Nachverfolgen von Änderungen werden zwei Revisionen angezeigt.
// Die „move from“-Revision ist eine Kopie des ursprünglichen Textes, bevor wir ihn verschoben haben.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Eine "Verschieben"-Revision:
// Die "move to"-Revision ist der Text, den wir an seine neue Position im Dokument verschoben haben.
// „Move from“- und „move to“-Revisionen erscheinen paarweise für jede Move-Revision, die wir durchführen.
// Das Akzeptieren einer Move-Revision löscht die "Move from"-Revision und ihren Text,
// und behält den Text aus der "move to"-Revision.
// Das Ablehnen einer Move-Revision behält umgekehrt die "Move from"-Revision und löscht die "Move to"-Revision.
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Eine "Lösch"-Revision:
// Diese Überarbeitung tritt auf, wenn wir Text löschen, während wir Änderungen nachverfolgen. Wenn wir solchen Text löschen,
// es bleibt als Überarbeitung im Dokument, bis wir entweder die Überarbeitung akzeptieren,
// wodurch der Text endgültig gelöscht wird, oder die Überarbeitung abgelehnt wird, wodurch der von uns gelöschte Text dort bleibt, wo er war.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Siehe auch

* class [InlineStory](../)
* namensraum [Aspose.Words](../../inlinestory/)
* Montage [Aspose.Words](../../../)


