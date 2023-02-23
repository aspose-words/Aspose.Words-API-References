---
title: Table.TextWrapping
linktitle: TextWrapping
second_title: Aspose.Words for .NET API Reference
description: Table property. Gets or sets TextWrapping for table in C#.
type: docs
weight: 310
url: /net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Gets or sets `TextWrapping` for table.

```csharp
public TextWrapping TextWrapping { get; set; }
```

## Examples

Shows how to work with table text wrapping.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
// and push it down into the paragraph below by setting the position.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### See Also

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
