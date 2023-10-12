---
title: Table.LastRow
second_title: Aspose.Words für .NET-API-Referenz
description: Table eigendom. Gibt den letzten zurückRow Knoten in der Tabelle.
type: docs
weight: 180
url: /de/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Gibt den letzten zurück[`Row`](../../row/) Knoten in der Tabelle.

```csharp
public Row LastRow { get; }
```

### Beispiele

Zeigt, wie die ersten und letzten Zeilen aller Tabellen in einem Dokument entfernt werden.

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

### Siehe auch

* class [Row](../../row/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


