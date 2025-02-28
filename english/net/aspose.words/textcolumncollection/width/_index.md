---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words for .NET
description: Discover the TextColumnCollection Width property: Easily manage evenly spaced columns for optimal layout and design in your projects.
type: docs
weight: 60
url: /net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

When columns are evenly spaced, gets the width of the columns.

```csharp
public double Width { get; }
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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
