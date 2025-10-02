---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Tables.PreferredWidth class, your solution for defining optimal table and cell widths with precision and flexibility. Enhance your document layouts today!
type: docs
weight: 7200
url: /net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell.

To learn more, visit the [Working with Tables](https://docs.aspose.com/words/net/working-with-tables/) documentation article.

```csharp
public sealed class PreferredWidth
```

## Properties

| Name | Description |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Gets the unit of measure used for this preferred width value. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Gets the preferred width value. The unit of measure is specified in the [`Type`](./type/) property. |

## Methods

| Name | Description |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | A creation method that returns a new instance that represents a preferred width specified as a percentage. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | A creation method that returns a new instance that represents a preferred width specified using a number of points. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | Determines whether the specified object is equal in value to the current object. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | Determines whether the specified `PreferredWidth` is equal in value to the current `PreferredWidth`. |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Serves as a hash function for this type. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Returns a user-friendly string that displays the value of this object. |

## Fields

| Name | Description |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | Returns an instance that represents the "preferred width is not specified" value. |

## Remarks

Preferred width can be specified as a percentage, number of points or a special "none/auto" value.

The instances of this class are immutable.

## Examples

Shows how to set a table to auto fit to 50% of the width of the page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
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

* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
