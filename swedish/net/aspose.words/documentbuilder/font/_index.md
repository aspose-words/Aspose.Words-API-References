---
title: DocumentBuilder.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: Utforska teckensnittsegenskapen i DocumentBuilder för att enkelt komma åt och anpassa din nuvarande teckensnittsformatering. Förbättra ditt dokuments stil idag!
type: docs
weight: 100
url: /sv/net/aspose.words/documentbuilder/font/
---
## DocumentBuilder.Font property

Returnerar ett objekt som representerar aktuella teckensnittsformateringsegenskaper.

```csharp
public Font Font { get; }
```

## Anmärkningar

Använda`Font` för att komma åt och ändra egenskaper för teckensnittsformatering.

Ange teckensnittsformatering innan du infogar text.

## Exempel

Visar hur man infogar en sträng omgiven av en kantlinje i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
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

* class [Font](../../font/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
