---
title: CellFormat.Width
second_title: Aspose.Words för .NET API Referens
description: CellFormat fast egendom. Får cellens bredd i punkter.
type: docs
weight: 140
url: /sv/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Får cellens bredd i punkter.

```csharp
public double Width { get; set; }
```

### Anmärkningar

Bredden beräknas av Aspose.Words om att ladda och spara dokument. För närvarande stöds inte alla kombinationer av tabell-, cell- och dokumentegenskaper. Det returnerade värdet kanske inte är korrekt för vissa dokument. Det kanske inte matchar exakt cellbredd beräknad av MS Word när dokumentet öppnas i MS Word.

Det rekommenderas inte att ställa in den här egenskapen. Det finns ingen garanti för att cellen faktiskt kommer att ha den inställda bredden. Bredden kan justeras för att passa cellinnehåll i en automatisk anpassningstabelllayout. Celler i andra rader kan ha motstridiga bredd settings. Tabellen kan ändras i storlek för att passa in i behållaren eller för att möta tabellbreddsinställningar. Överväg att använda[`PreferredWidth`](../preferredwidth/) för att ställa in cellbredden. Inställning av denna egenskapsuppsättning[`PreferredWidth`](../preferredwidth/)implicit sedan version 15.8.

### Exempel

Visar hur man formaterar celler med en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Infoga en andra cell och konfigurera sedan utfyllnadsalternativ för celltext.
// Byggaren kommer att tillämpa dessa inställningar på sin nuvarande cell, och alla nya celler skapas efteråt.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// Den första cellen påverkades inte av utfyllnadsomställningen och har fortfarande standardvärdena.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// Den första cellen kommer fortfarande att växa i utdatadokumentet för att matcha storleken på dess närliggande cell.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
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

* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../cellformat/)
* hopsättning [Aspose.Words](../../../)


