---
title: Border Class
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Border class. Represents a border of an object in C#.
type: docs
weight: 70
url: /net/aspose.words/border/
---
## Border class

Represents a border of an object.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class Border : InternableComplexAttr
```

## Properties

| Name | Description |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Gets or sets the border color. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Gets or sets distance of the border from text or from the page edge in points. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Returns `true` if the [`LineStyle`](./linestyle/) is not None. |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Gets or sets the border style. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Gets or sets the border width in points. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Gets or sets a value indicating whether the border has a shadow. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Gets or sets the theme color in the applied color scheme that is associated with this Border object. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Gets or sets a double value that lightens or darkens a color. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Resets border properties to default values. |
| [Equals](../../aspose.words/border/equals/#equals)(Border) | Determines whether the specified border is equal in value to the current border. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(object) | Determines whether the specified object is equal in value to the current object. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Serves as a hash function for this type. |

## Remarks

Borders can be applied to various document elements including paragraph, run of text inside a paragraph or a table cell.

## Examples

Shows how to insert a string surrounded by a border into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

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

* class [InternableComplexAttr](../internablecomplexattr/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
