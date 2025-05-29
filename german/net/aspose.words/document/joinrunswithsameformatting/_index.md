---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Methode JoinRunsWithSameFormatting formatierten Text nahtlos in die Absätze Ihres Dokuments einfügt und so für ein elegantes, professionelles Erscheinungsbild sorgt.
type: docs
weight: 660
url: /de/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Verknüpfungen werden mit der gleichen Formatierung in allen Absätzen des Dokuments ausgeführt.

```csharp
public int JoinRunsWithSameFormatting()
```

### Rückgabewert

Anzahl der durchgeführten Verknüpfungen. Wann**N** Wenn benachbarte Läufe verbunden werden, zählen sie als**N - 1** schließt sich an.

## Bemerkungen

Dies ist eine Optimierungsmethode. Einige Dokumente enthalten nebeneinanderliegende Läufe mit gleicher Formatierung. Dies tritt normalerweise auf, wenn ein Dokument intensiv manuell bearbeitet wurde. Durch das Zusammenführen dieser Läufe können Sie die Dokumentgröße reduzieren und die weitere Verarbeitung beschleunigen.

Die Operation prüft jeden[`Paragraph`](../../paragraph/) Knoten im Dokument für benachbarte[`Run`](../../run/) -Knoten mit identischen Eigenschaften. Eindeutige Kennungen zur Verfolgung von Bearbeitungssitzungen bei der Erstellung und Änderung von run werden ignoriert. Der erste Lauf in jeder Verbindungssequenz sammelt den gesamten Text. Verbleibende -Läufe werden aus dem Dokument gelöscht.

## Beispiele

Zeigt, wie Läufe in einem Dokument verbunden werden, um unnötige Läufe zu reduzieren.

```csharp
// Öffnen Sie ein Dokument, das nebeneinander liegende Textabschnitte mit identischer Formatierung enthält.
// was häufig auftritt, wenn wir denselben Absatz in Microsoft Word mehrmals bearbeiten.
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn eine beliebige Anzahl dieser Läufe mit identischer Formatierung nebeneinander liegt,
// dann kann das Dokument vereinfacht werden.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Kombinieren Sie solche Läufe mit dieser Methode und überprüfen Sie die Anzahl der stattfindenden Laufverknüpfungen.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// Die Anzahl der Joins und die Anzahl der Runs, die wir nach dem Join haben
// sollte die Anzahl der Läufe addieren, die wir anfangs hatten.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
