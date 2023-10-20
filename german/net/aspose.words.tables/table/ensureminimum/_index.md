---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words für .NET
description: Table EnsureMinimum methode. Wenn die Tabelle keine Zeilen enthält wird eine erstellt und angehängtRow  in C#.
type: docs
weight: 400
url: /de/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Wenn die Tabelle keine Zeilen enthält, wird eine erstellt und angehängt[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Beispiele

Zeigt, wie sichergestellt wird, dass ein Tabellenknoten die Knoten enthält, die wir zum Hinzufügen von Inhalten benötigen.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die Absätze enthalten können
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Unsere neue Tabelle hat keinen dieser Knoten und wir können ihr erst dann Inhalte hinzufügen, wenn dies der Fall ist.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Der Aufruf der Methode „EnsureMinimum“ für eine Tabelle stellt dies sicher
// Die Tabelle enthält mindestens eine Zeile und eine Zelle mit einem leeren Absatz.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
