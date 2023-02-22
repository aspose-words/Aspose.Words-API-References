---
title: Table.EnsureMinimum
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Wenn die Tabelle keine Zeilen hat wird eine erstellt und angehängt Die Zeile .
type: docs
weight: 400
url: /de/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Wenn die Tabelle keine Zeilen hat, wird eine erstellt und angehängt **Die Zeile** .

```csharp
public void EnsureMinimum()
```

### Beispiele

Zeigt, wie sichergestellt wird, dass ein Tabellenknoten die Knoten enthält, die wir zum Hinzufügen von Inhalten benötigen.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die Absätze enthalten können
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Unsere neue Tabelle hat keinen dieser Knoten, und wir können ihr keinen Inhalt hinzufügen, bis dies der Fall ist.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Das Aufrufen der "EnsureMinimum"-Methode für eine Tabelle stellt dies sicher
// Die Tabelle hat mindestens eine Zeile und eine Zelle mit einem leeren Absatz.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


