---
title: Table.FirstRow
linktitle: FirstRow
articleTitle: FirstRow
second_title: Aspose.Words för .NET
description: Upptäck FirstRow-egenskapen för tabeller, få enkel åtkomst till den första radens nod för effektiv datahantering och förbättrad tabellfunktionalitet.
type: docs
weight: 160
url: /sv/net/aspose.words.tables/table/firstrow/
---
## Table.FirstRow property

Returnerar det första[`Row`](../../row/) nod i tabellen.

```csharp
public Row FirstRow { get; }
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

Visar hur man kombinerar rader från två tabeller till en.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nedan följer två sätt att hämta en tabell från ett dokument.
// 1 - Från samlingen "Tabeller" i en Body-nod:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Använda metoden "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Lägger till alla rader från den aktuella tabellen till nästa.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Ta bort den tomma tabellbehållaren.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Se även

* class [Row](../../row/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
