---
title: Table.FirstRow
linktitle: FirstRow
articleTitle: FirstRow
second_title: Aspose.Words für .NET
description: Entdecken Sie die FirstRow-Eigenschaft von Tabellen und greifen Sie mühelos auf den Knoten der ersten Zeile zu, um die Datenverwaltung zu optimieren und die Tabellenfunktionalität zu verbessern.
type: docs
weight: 160
url: /de/net/aspose.words.tables/table/firstrow/
---
## Table.FirstRow property

Gibt den ersten[`Row`](../../row/) Knoten in der Tabelle.

```csharp
public Row FirstRow { get; }
```

## Beispiele

Zeigt, wie die erste und die letzte Zeile aller Tabellen in einem Dokument entfernt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

Zeigt, wie die Zeilen aus zwei Tabellen zu einer kombiniert werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Unten sind zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
// 1 – Aus der „Tabellen“-Sammlung eines Body-Knotens:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Verwenden der Methode „GetChild“:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Alle Zeilen der aktuellen Tabelle an die nächste anhängen.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Entfernen Sie den leeren Tabellencontainer.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Siehe auch

* class [Row](../../row/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
