---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table LastRow för att enkelt komma åt den sista radnoden i din tabell, vilket förbättrar datahanteringen och effektiviteten.
type: docs
weight: 180
url: /sv/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Returnerar det sista[`Row`](../../row/) nod i tabellen.

```csharp
public Row LastRow { get; }
```

## Exempel

Visar hur man tar bort den första och sista raden i alla tabeller i ett dokument.

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

### Se även

* class [Row](../../row/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
