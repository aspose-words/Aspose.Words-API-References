---
title: BorderCollection.Bottom
second_title: Aspose.Words for .NET API Reference
description: BorderCollection property. Gets the bottom border in C#.
type: docs
weight: 10
url: /net/aspose.words/bordercollection/bottom/
---
## BorderCollection.Bottom property

Gets the bottom border.

```csharp
public Border Bottom { get; }
```

## Examples

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

* class [Border](../../border/)
* class [BorderCollection](../)
* namespace [Aspose.Words](../../bordercollection/)
* assembly [Aspose.Words](../../../)
