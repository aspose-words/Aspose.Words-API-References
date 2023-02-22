---
title: Table.AllowCellSpacing
second_title: Aspose.Words för .NET API Referens
description: Table fast egendom. Hämtar eller ställer in alternativet Tillåt avstånd mellan celler.
type: docs
weight: 60
url: /sv/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

Hämtar eller ställer in alternativet "Tillåt avstånd mellan celler".

```csharp
public bool AllowCellSpacing { get; set; }
```

### Exempel

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

// Ställ in egenskapen "AllowCellSpacing" till "true" för att möjliggöra avstånd mellan celler
// med en magnitud lika med värdet på egenskapen "CellSpacing", i poäng.
// Ställ in egenskapen "AllowCellSpacing" till "false" för att inaktivera cellavstånd
// och ignorera värdet för egenskapen "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// Om du justerar egenskapen "CellSpacing" aktiveras cellavstånd automatiskt.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../table/)
* hopsättning [Aspose.Words](../../../)


