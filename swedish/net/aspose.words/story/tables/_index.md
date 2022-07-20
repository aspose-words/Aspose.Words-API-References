---
title: Tables
second_title: Aspose.Words för .NET API Referens
description: Får en samling tabeller som är omedelbara barn till berättelsen.
type: docs
weight: 50
url: /sv/net/aspose.words/story/tables/
---
## Story.Tables property

Får en samling tabeller som är omedelbara barn till berättelsen.

```csharp
public TableCollection Tables { get; }
```

### Exempel

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

* class [TableCollection](../../../aspose.words.tables/tablecollection)
* class [Story](../../story)
* namnutrymme [Aspose.Words](../../story)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->