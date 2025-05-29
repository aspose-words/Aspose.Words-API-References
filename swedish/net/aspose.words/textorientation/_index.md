---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TextOrientation enum för att enkelt kontrollera textjustering i tabellceller och textramar, vilket förbättrar dokumentpresentationen och läsbarheten.
type: docs
weight: 7280
url: /sv/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Anger textens orientering på en sida, i en tabellcell eller en textram.

```csharp
public enum TextOrientation
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Horizontal | `0` | Texten är ordnad horisontellt (l-tb). |
| Downward | `1` | Texten roteras 90 grader åt höger för att visas uppifrån och ned (tb-rl). |
| Upward | `3` | Texten roteras 90 grader åt vänster för att visas nerifrån och upp (bt-lr). |
| HorizontalRotatedFarEast | `4` | Texten är ordnad horisontellt, men tecken från Fjärran Östern är roterade 90 grader åt vänster (lr-tb-v). |
| VerticalFarEast | `5` | Tecken från Fjärran Östern visas vertikalt, annan text roteras 90 grader åt höger för att visas uppifrån och ned (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Tecken från Fjärran Östern visas vertikalt, annan text roteras 90 grader åt höger för att visas uppifrån och ned vertikalt, sedan från vänster till höger horisontellt (tb-lr-v). |

## Exempel

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
