---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words for .NET
description: Aspose.Words.TextColumn class. Represents a single text column. TextColumn is a member of the TextColumnCollection collection. The TextColumn collection includes all the columns in a section of a document in C#.
type: docs
weight: 6900
url: /net/aspose.words/textcolumn/
---
## TextColumn class

Represents a single text column. `TextColumn` is a member of the [`TextColumnCollection`](../textcolumncollection/) collection. The `TextColumn` collection includes all the columns in a section of a document.

To learn more, visit the [Working with Sections](https://docs.aspose.com/words/net/working-with-sections/) documentation article.

```csharp
public class TextColumn
```

## Properties

| Name | Description |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Gets or sets the space between this column and the next column in points. Not required for the last column. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Gets or sets the width of the text column in points. |

## Remarks

`TextColumn` objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) to `true`.

When a new `TextColumn` is created it has its width and spacing set to zero.

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
