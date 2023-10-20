---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words für .NET
description: Cell EnsureMinimum methode. Wenn das letzte untergeordnete Element kein Absatz ist wird ein leerer Absatz erstellt und angehängt in C#.
type: docs
weight: 140
url: /de/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Wenn das letzte untergeordnete Element kein Absatz ist, wird ein leerer Absatz erstellt und angehängt.

```csharp
public void EnsureMinimum()
```

## Beispiele

Zeigt, wie sichergestellt wird, dass ein Zellknoten die Knoten enthält, die wir benötigen, um mit dem Hinzufügen von Inhalten zu beginnen.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Zellen können Absätze mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen enthalten.
// Unsere neue Zelle hat keine Absätze und wir können ihr erst dann Inhalte wie Lauf- und Formknoten hinzufügen, wenn dies der Fall ist.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// Durch Aufrufen der Methode „EnsureMinimum“ für eine Zelle wird dies sichergestellt
// Die Zelle hat mindestens einen leeren Absatz, dem wir dann Inhalte hinzufügen können.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Cell](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
