---
title: RowFormat.HeightRule
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RowFormat HeightRule för att enkelt anpassa tabellradhöjder för optimal layout och design i dina applikationer.
type: docs
weight: 50
url: /sv/net/aspose.words.tables/rowformat/heightrule/
---
## RowFormat.HeightRule property

Hämtar eller ställer in regeln för att bestämma höjden på tabellraden.

```csharp
public HeightRule HeightRule { get; set; }
```

## Exempel

Visar hur man formaterar rader med en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Starta en andra rad och konfigurera sedan dess höjd. Byggaren kommer att tillämpa dessa inställningar på
// dess nuvarande rad, såväl som alla nya rader som skapas efteråt.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Den första raden påverkades inte av omkonfigureringen av utfyllnaden och har fortfarande standardvärdena.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

Visar hur man skapar en formaterad tabell med hjälp av DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Ange några formateringsalternativ för text och tabellutseende.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Att konfigurera formateringsalternativen i en dokumentbyggare kommer att tillämpa dem
// till den aktuella cellen/raden där markören befinner sig,
// såväl som alla nya celler och rader som skapats med den verktygsbyggaren.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Konfigurera om formateringsobjekten i verktyget för nya rader och celler som vi ska skapa.
// Skaparen kommer inte att tillämpa dessa på den första raden som redan skapats så att den kommer att synas som en rubrikrad.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Se även

* enum [HeightRule](../../../aspose.words/heightrule/)
* class [RowFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
