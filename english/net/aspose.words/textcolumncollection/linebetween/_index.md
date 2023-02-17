---
title: TextColumnCollection.LineBetween
second_title: Aspose.Words for .NET API Reference
description: TextColumnCollection property. When true adds a vertical line between columns in C#.
type: docs
weight: 40
url: /net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

When `true`, adds a vertical line between columns.

```csharp
public bool LineBetween { get; set; }
```

## Examples

Shows how to separate columns with a vertical line.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configure the current section's PageSetup object to divide the text into several columns.
// Set the "LineBetween" property to "true" to put a dividing line between columns.
// Set the "LineBetween" property to "false" to leave the space between columns blank.
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.LineBetween = lineBetween;
columns.SetCount(3);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 3.");

doc.Save(ArtifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### See Also

* class [TextColumnCollection](../)
* namespace [Aspose.Words](../../textcolumncollection/)
* assembly [Aspose.Words](../../../)
