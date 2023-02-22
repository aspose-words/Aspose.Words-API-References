---
title: Table.LeftIndent
second_title: Aspose.Words för .NET API Referens
description: Table fast egendom. Hämtar eller ställer in värdet som representerar den vänstra indraget i tabellen.
type: docs
weight: 190
url: /sv/net/aspose.words.tables/table/leftindent/
---
## Table.LeftIndent property

Hämtar eller ställer in värdet som representerar den vänstra indraget i tabellen.

```csharp
public double LeftIndent { get; set; }
```

### Exempel

Visar hur man skapar en formaterad tabell med DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Ställ in några formateringsalternativ för text och tabellutseende.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Konfigurering av formateringsalternativen i en dokumentbyggare kommer att tillämpa dem
// till den aktuella cellen/raden dess markör är i,
// samt eventuella nya celler och rader skapade med hjälp av den byggaren.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Konfigurera om byggarens formateringsobjekt för nya rader och celler som vi håller på att göra.
// Byggaren kommer inte att tillämpa dessa på den första raden som redan skapats så att den kommer att sticka ut som en rubrikrad.
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

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../table/)
* hopsättning [Aspose.Words](../../../)


