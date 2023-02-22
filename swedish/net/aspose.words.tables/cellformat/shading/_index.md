---
title: CellFormat.Shading
second_title: Aspose.Words för .NET API Referens
description: CellFormat fast egendom. Returnerar ett Shadingobjekt som refererar till skuggformateringen för cellen.
type: docs
weight: 90
url: /sv/net/aspose.words.tables/cellformat/shading/
---
## CellFormat.Shading property

Returnerar ett Shading-objekt som refererar till skuggformateringen för cellen.

```csharp
public Shading Shading { get; }
```

### Exempel

Visar hur du ändrar formatet för rader och celler i en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Använd den första radens "RowFormat"-egenskap för att ändra formateringen
// av innehållet i alla celler i den här raden.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Använd egenskapen "CellFormat" för den första cellen i den sista raden för att ändra formateringen av cellens innehåll.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

Visar hur man bygger en tabell med anpassade ramar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Ställa in tabellformateringsalternativ för en dokumentbyggare
// kommer att tillämpa dem på varje rad och cell som vi lägger till med den.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Ändring av formateringen kommer att tillämpa den på den aktuella cellen,
// och eventuella nya celler som vi skapar med byggaren efteråt.
// Detta kommer inte att påverka cellerna som vi har lagt till tidigare.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Öka radhöjden så att den passar den vertikala texten.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Se även

* class [Shading](../../../aspose.words/shading/)
* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../cellformat/)
* hopsättning [Aspose.Words](../../../)


