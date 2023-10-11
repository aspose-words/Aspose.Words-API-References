---
title: Document.JoinRunsWithSameFormatting
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Joins werden in allen Absätzen des Dokuments mit der gleichen Formatierung ausgeführt.
type: docs
weight: 640
url: /de/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Joins werden in allen Absätzen des Dokuments mit der gleichen Formatierung ausgeführt.

```csharp
public int JoinRunsWithSameFormatting()
```

### Rückgabewert

Anzahl der durchgeführten Joins. Wann **N** Benachbarte Läufe werden zusammengefügt, sie zählen als **N - 1** schließt sich an.

### Bemerkungen

Dies ist eine Optimierungsmethode. Einige Dokumente enthalten benachbarte Läufe mit derselben Formatierung. Dies tritt normalerweise auf, wenn ein Dokument intensiv manuell bearbeitet wurde. Sie können die Dokumentgröße reduzieren und die weitere Verarbeitung beschleunigen, indem Sie diese Läufe zusammenfügen.

Der Betrieb prüft alle[`Paragraph`](../../paragraph/) Knoten im Dokument für angrenzend[`Run`](../../run/) Knoten mit identischen Eigenschaften. Es ignoriert eindeutige Bezeichner, die zum Verfolgen von Bearbeitungssitzungen zur Erstellung und Änderung von run verwendet werden. Beim ersten Durchlauf in jeder Verbindungssequenz wird der gesamte Text akkumuliert. Verbleibende Läufe werden aus dem Dokument gelöscht.

### Beispiele

Zeigt, wie Läufe in einem Dokument zusammengefügt werden, um unnötige Läufe zu reduzieren.

```csharp
// Öffnen Sie ein Dokument, das benachbarte Textabschnitte mit identischer Formatierung enthält.
// was häufig auftritt, wenn wir denselben Absatz mehrmals in Microsoft Word bearbeiten.
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn beliebig viele dieser Läufe mit identischer Formatierung nebeneinander liegen,
// dann kann das Dokument vereinfacht werden.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Solche Läufe mit dieser Methode kombinieren und die Anzahl der stattfindenden Laufverknüpfungen überprüfen.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// Die Anzahl der Joins und die Anzahl der Läufe, die wir nach dem Join haben
// sollte die Anzahl der Läufe addieren, die wir ursprünglich hatten.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


