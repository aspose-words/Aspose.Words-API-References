---
title: Table.SetBorders
linktitle: SetBorders
second_title: Aspose.Words for .NET API Reference
description: Table method. Sets all table borders to the specified line style width and color in C#.
type: docs
weight: 420
url: /net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Sets all table borders to the specified line style, width and color.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Parameter | Type | Description |
| --- | --- | --- |
| lineStyle | LineStyle | The line style to apply. |
| lineWidth | Double | The line width to set (in points). |
| color | Color | The color to use for the border. |

## Examples

Shows how to format of all of a table's borders at once.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Clear all existing borders from the table.
table.ClearBorders();

// Set a single green line to serve as every outer and inner border of this table.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

Shows how to apply border and shading color while building a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Start a table and set a default color/thickness for its borders.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Create a row with two cells with different background colors.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Reset cell formatting to disable the background colors
// set a custom border thickness for all new cells created by the builder,
// then build a second row.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### See Also

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
