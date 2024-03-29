---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words för .NET
description: Table AllowAutoFit fast egendom. Tillåter Microsoft Word och Aspose.Words att automatiskt ändra storlek på celler i en tabell så att de passar deras innehåll i C#.
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

Standardvärdet är`Sann`.

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

// Ställ in egenskapen "AllowAutoFit" till "false" för att få tabellen att behålla dimensionerna
// av alla dess rader och celler, och trunkera innehållet om de blir för stora för att passa.
// Ställ in egenskapen "AllowAutoFit" till "true" för att tillåta tabellen att ändra cellernas bredd och höjd
// för att tillgodose deras innehåll.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
