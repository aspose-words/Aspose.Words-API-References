---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „Table EnsureMinimum“, mit der Sie mühelos eine Zeile erstellen und anhängen können, wenn Ihre Tabelle leer ist, um eine nahtlose Datenverwaltung zu gewährleisten.
type: docs
weight: 420
url: /de/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Wenn die Tabelle keine Zeilen hat, wird eine erstellt und angehängt[`Row`](../../row/) .

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
// Unsere neue Tabelle hat keinen dieser Knoten und wir können ihr keine Inhalte hinzufügen, bis sie welche hat.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Der Aufruf der Methode "EnsureMinimum" für eine Tabelle stellt sicher, dass
// Die Tabelle hat mindestens eine Zeile und eine Zelle mit einem leeren Absatz.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
