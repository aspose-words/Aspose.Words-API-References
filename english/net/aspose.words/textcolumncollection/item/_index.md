---
title: TextColumnCollection.Item
linktitle: Item
second_title: Aspose.Words for .NET API Reference
description: TextColumnCollection Item property. Returns a text column at the specified index in C#.
type: docs
weight: 30
url: /net/aspose.words/textcolumncollection/item/
---
## TextColumnCollection indexer

Returns a text column at the specified index.

```csharp
public TextColumn this[int index] { get; }
```

## Examples

Shows how to create unevenly spaced columns.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Determine the amount of room that we have available for arranging columns.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Set the first column to be narrow.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Set the second column to take the rest of the space available within the margins of the page.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### See Also

* class [TextColumn](../../textcolumn/)
* class [TextColumnCollection](../)
* namespace [Aspose.Words](../../textcolumncollection/)
* assembly [Aspose.Words](../../../)
