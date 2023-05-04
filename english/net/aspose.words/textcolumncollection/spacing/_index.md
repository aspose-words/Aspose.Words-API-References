---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words for .NET
description: TextColumnCollection Spacing property. When columns are evenly spaced gets or sets the amount of space between each column in points in C#.
type: docs
weight: 50
url: /net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

When columns are evenly spaced, gets or sets the amount of space between each column in points.

```csharp
public double Spacing { get; set; }
```

## Remarks

Has effect only when [`EvenlySpaced`](../evenlyspaced/) is set to `true`.

## Examples

Shows how to create multiple evenly spaced columns in a section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### See Also

* class [TextColumnCollection](../)
* namespace [Aspose.Words](../../textcolumncollection/)
* assembly [Aspose.Words](../../../)
