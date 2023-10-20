---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words för .NET
description: Aspose.Words.TextOrientation uppräkning. Anger orientering av text på en sida i en tabellcell eller en textram i C#.
type: docs
weight: 6430
url: /sv/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Anger orientering av text på en sida, i en tabellcell eller en textram.

```csharp
public enum TextOrientation
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Horizontal | `0` | Texten är anordnad horisontellt (lr-tb). |
| Downward | `1` | Text roteras 90 grader åt höger för att visas uppifrån och ned (tb-rl). |
| Upward | `3` | Text roteras 90 grader åt vänster för att visas från botten till toppen (bt-lr). |
| HorizontalRotatedFarEast | `4` | Texten är ordnad horisontellt, men Fjärran Östern-tecken roteras 90 grader åt vänster (lr-tb-v). |
| VerticalFarEast | `5` | Fjärran Östern-tecken visas vertikala, annan text roteras 90 grader till höger för att visas uppifrån och ned (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Fjärran Östern-tecken visas vertikala, annan text roteras 90 grader åt höger för att visas uppifrån och ned vertikalt, sedan från vänster till höger horisontellt (tb-lr-v). |

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

// När du bygger tabellen kommer dokumentbyggaren att tillämpa sina nuvarande RowFormat/CellFormat-egenskapsvärden
// till den aktuella raden/cellen som markören är i och eventuella nya rader/celler när den skapar dem.
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

// Tidigare tillagda rader och celler påverkas inte retroaktivt av ändringar i byggarens formatering.
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
