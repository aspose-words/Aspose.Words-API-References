---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: Aspose.Words for .NET
description: Explore Aspose.Words.TextColumnCollection to manage text columns in your documents effortlessly. Enhance your document formatting with ease!
type: docs
weight: 7260
url: /net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

A collection of [`TextColumn`](../textcolumn/) objects that represent all the columns of text in a section of a document.

To learn more, visit the [Working with Sections](https://docs.aspose.com/words/net/working-with-sections/) documentation article.

```csharp
public class TextColumnCollection
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Gets the number of columns in the section of a document. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | True if text columns are of equal width and evenly spaced. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Returns a text column at the specified index. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | When `true`, adds a vertical line between columns. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | When columns are evenly spaced, gets or sets the amount of space between each column in points. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | When columns are evenly spaced, gets the width of the columns. |

## Methods

| Name | Description |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | Arranges text into the specified number of text columns. |

## Remarks

Use [`SetCount`](./setcount/) to set the number of text columns.

To make all columns equal width and spaced evenly, set [`EvenlySpaced`](./evenlyspaced/) to `true` and specify the amount of space between the columns in [`Spacing`](./spacing/). MS Word will automatically calculate column widths.

If you have [`EvenlySpaced`](./evenlyspaced/) set to `false`, you need to specify width and spacing for each column individually. Use the indexer to access individual [`TextColumn`](../textcolumn/) objects.

When using custom column widths, make sure the sum of all column widths and spacings between them equals page width minus left and right page margins.

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
