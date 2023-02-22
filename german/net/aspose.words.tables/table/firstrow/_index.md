---
title: Table.FirstRow
second_title: Aspose.Words für .NET-API-Referenz
description: Table eigendom. Gibt den ersten zurück Die Zeile Knoten in der Tabelle.
type: docs
weight: 160
url: /de/net/aspose.words.tables/table/firstrow/
---
## Table.FirstRow property

Gibt den ersten zurück **Die Zeile** Knoten in der Tabelle.

```csharp
public Row FirstRow { get; }
```

### Beispiele

Zeigt, wie die erste und letzte Zeile aller Tabellen in einem Dokument entfernt werden.

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

// Im Folgenden finden Sie zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
// 1 - Aus der "Tables"-Sammlung eines Body-Knotens:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Verwendung der "GetChild"-Methode:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Alle Zeilen der aktuellen Tabelle an die nächste anhängen.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Entferne den leeren Tabellencontainer.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Siehe auch

* class [Row](../../row/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


