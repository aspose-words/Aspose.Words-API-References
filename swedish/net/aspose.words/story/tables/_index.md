---
title: Story.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words för .NET
description: Upptäck Story Tables, en kurerad samling tabeller direkt kopplade till din berättelse, som enkelt förbättrar organisation och engagemang.
type: docs
weight: 50
url: /sv/net/aspose.words/story/tables/
---
## Story.Tables property

Hämtar en samling tabeller som är direkta underordnade tabeller till berättelsen.

```csharp
public TableCollection Tables { get; }
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

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [Story](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
