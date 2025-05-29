---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
articleTitle: AutoFitBehavior
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Tables.AutoFitBehavior enum för att optimera tabellstorleksändring med AutoFit-metoden, vilket förbättrar dokumentlayout och presentation.
type: docs
weight: 7080
url: /sv/net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

Bestämmer hur Aspose.Words ändrar storlek på tabellen när du anropar[`AutoFit`](../table/autofit/) metod.

```csharp
public enum AutoFitBehavior
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| AutoFitToContents | `0` | Aspose.Words aktiverar alternativet Autopassning, tar bort önskad bredd från tabellen och alla celler och uppdaterar sedan tabelllayouten. |
| AutoFitToWindow | `1` | När du använder det här värdet aktiverar Aspose.Words alternativet Autopassning, ställer in önskad bredd för tabellen till 100 %, tar bort önskade bredder från alla celler och uppdaterar sedan tabelllayouten. |
| FixedColumnWidths | `2` | Aspose.Words inaktiverar alternativet Autopassning och tar bort den föredragna with från tabellen. |

## Exempel

Visar hur man skapar en ny tabell samtidigt som man tillämpar en stil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Vi måste infoga minst en rad innan vi anger någon tabellformatering.
builder.InsertCell();

// Ange tabellstilen som används baserat på stilidentifieraren.
// Observera att inte alla tabellformat är tillgängliga när man sparar i .doc-format.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Tillämpa delvis stilen på tabellens funktioner baserat på predikat, och bygg sedan tabellen.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

Visar hur man bygger en formaterad 2x2-tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// När tabellen skapas kommer dokumentbyggaren att tillämpa dess aktuella RowFormat/CellFormat-egenskapsvärden
// till den aktuella raden/cellen där markören befinner sig och alla nya rader/celler allt eftersom de skapas.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Tidigare tillagda rader och celler påverkas inte retroaktivt av ändringar i formateringen i verktyget.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Se även

* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
