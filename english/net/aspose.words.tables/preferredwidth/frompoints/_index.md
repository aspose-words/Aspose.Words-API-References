---
title: PreferredWidth.FromPoints
linktitle: FromPoints
articleTitle: FromPoints
second_title: Aspose.Words for .NET
description: Discover the PreferredWidth FromPoints method to create a new instance with a defined width in points, enhancing your design precision and efficiency.
type: docs
weight: 30
url: /net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

A creation method that returns a new instance that represents a preferred width specified using a number of points.

```csharp
public static PreferredWidth FromPoints(double points)
```

| Parameter | Type | Description |
| --- | --- | --- |
| points | Double | The value must be from 0 to 22 inches (22 * 72 points). |

## Examples

Shows how to use unit conversion tools while specifying a preferred width for a cell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(ConvertUtil.InchToPoint(3));
builder.InsertCell();

Assert.That(table.FirstRow.FirstCell.CellFormat.PreferredWidth.Value, Is.EqualTo(216.0d));
```

Shows how to set a preferred width for table cells.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// There are two ways of applying the "PreferredWidth" class to table cells.
// 1 -  Set an absolute preferred width based on points:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 -  Set a relative preferred width based on percent of the table's width:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// A cell with no preferred width specified will take up the rest of the available space.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Each configuration of the "PreferredWidth" property creates a new object.
Assert.That(builder.CellFormat.PreferredWidth.GetHashCode(), Is.Not.EqualTo(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode()));

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### See Also

* class [PreferredWidth](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
