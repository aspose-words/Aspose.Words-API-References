---
title: Table.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words for .NET
description: Discover the Table TopPadding property, easily adjust space in points above cell contents for enhanced layout control and improved readability.
type: docs
weight: 330
url: /net/aspose.words.tables/table/toppadding/
---
## Table.TopPadding property

Gets or sets the amount of space (in points) to add above the contents of cells.

```csharp
public double TopPadding { get; set; }
```

## Examples

Shows how to configure content padding in a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

// For every cell in the table, set the distance between its contents and each of its borders. 
// This table will maintain the minimum padding distance by wrapping text.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### See Also

* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
