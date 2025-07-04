---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: Aspose.Words for .NET
description: Explore Aspose.Words.BorderCollection, your go-to solution for managing and customizing Border objects effortlessly for enhanced document formatting.
type: docs
weight: 270
url: /net/aspose.words/bordercollection/
---
## BorderCollection class

A collection of [`Border`](../border/) objects.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Properties

| Name | Description |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Gets the bottom border. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Gets or sets the border color. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Gets the number of borders in the collection. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Gets or sets distance of the border from text in points. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Gets the horizontal border that is used between cells or conforming paragraphs. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Retrieves a [`Border`](../border/) object by border type. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Gets the left border. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Gets or sets the border style. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Gets or sets the border width in points. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Gets the right border. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Gets or sets a value indicating whether the border has a shadow. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Gets the top border. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Gets the vertical border that is used between cells. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Removes all borders of an object. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | Compares collections of borders. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all borders in the collection. |

## Remarks

Different document elements have different borders. For example, [`ParagraphFormat`](../paragraphformat/) has [`Bottom`](./bottom/), [`Left`](./left/), [`Right`](./right/) and [`Top`](./top/) borders. You can specify different formatting for each border independently or enumerate through all borders and apply same formatting.

## Examples

Shows how to insert a paragraph with a top border.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Set ThemeColor only when LineWidth or LineStyle setted.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### See Also

* class [Border](../border/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
