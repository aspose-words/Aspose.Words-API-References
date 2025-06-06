---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table AllowCellSpacing för att enkelt hantera cellavstånd i dina layouter. Förbättra din design med anpassningsbara alternativ!
type: docs
weight: 60
url: /sv/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

Hämtar eller ställer in alternativet "Tillåt avstånd mellan celler".

```csharp
public bool AllowCellSpacing { get; set; }
```

## Exempel

Visar hur man aktiverar avstånd mellan enskilda celler i en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Sätt egenskapen "AllowCellSpacing" till "true" för att aktivera avstånd mellan celler
// med en magnitud lika med värdet av egenskapen "CellSpacing", i punkter.
// Sätt egenskapen "AllowCellSpacing" till "false" för att inaktivera cellavstånd
// och ignorera värdet för egenskapen "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// Om du justerar egenskapen "CellSpacing" aktiveras cellavståndet automatiskt.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
