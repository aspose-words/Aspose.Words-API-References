---
title: Table.AbsoluteVerticalDistance
linktitle: AbsoluteVerticalDistance
second_title: Aspose.Words for .NET API Reference
description: Table property. Gets or sets absolute vertical floating table position specified by the table properties in points. Default value is 0 in C#.
type: docs
weight: 30
url: /net/aspose.words.tables/table/absoluteverticaldistance/
---
## Table.AbsoluteVerticalDistance property

Gets or sets absolute vertical floating table position specified by the table properties, in points. Default value is 0.

```csharp
public double AbsoluteVerticalDistance { get; set; }
```

## Examples

Shows how set the location of floating tables.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Set the table's location to a place on the page, such as, in this case, the bottom right corner.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table. 
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### See Also

* class [Table](../)
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
