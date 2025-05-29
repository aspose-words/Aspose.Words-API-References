---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table AllowAutoFit för att enkelt ändra storlek på tabellceller i Microsoft Word och Aspose.Words, vilket förbättrar dokumentets läsbarhet och presentation.
type: docs
weight: 50
url: /sv/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Tillåter Microsoft Word och Aspose.Words att automatiskt ändra storlek på celler i en tabell så att de passar deras innehåll.

```csharp
public bool AllowAutoFit { get; set; }
```

## Anmärkningar

Standardvärdet är`sann`.

## Exempel

Visar hur man aktiverar/inaktiverar automatisk storleksändring av tabellceller.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// Sätt egenskapen "AllowAutoFit" till "false" för att tabellen ska bibehålla måtten
// av alla dess rader och celler, och avkorta innehållet om det blir för stort för att få plats.
// Sätt egenskapen "AllowAutoFit" till "true" för att tillåta att tabellen ändrar cellernas bredd och höjd
// för att rymma deras innehåll.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
