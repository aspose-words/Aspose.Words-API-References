---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Shading class, designed to enhance your documents with customizable shading attributes for a professional look.
type: docs
weight: 6860
url: /net/aspose.words/shading/
---
## Shading class

Contains shading attributes for an object.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class Shading : InternableComplexAttr
```

## Properties

| Name | Description |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Gets or sets the color that's applied to the background of the `Shading` object. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Gets or sets the background pattern theme color in the applied color scheme that is associated with this `Shading` object. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Gets or sets a double value that lightens or darkens a background theme color. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Gets or sets the color that's applied to the foreground of the `Shading` object. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Gets or sets the foreground pattern theme color in the applied color scheme that is associated with this `Shading` object. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Gets or sets a double value that lightens or darkens a foreground theme color. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Gets or sets the shading texture. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Removes shading from the object. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Determines whether the specified object is equal in value to the current object. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Determines whether the specified `Shading` is equal in value to the current `Shading`. |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Serves as a hash function for this type. |

## Examples

Shows how to decorate text with borders and shading.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

Shows how to apply border and shading color while building a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Start a table and set a default color/thickness for its borders.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Create a row with two cells with different background colors.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Reset cell formatting to disable the background colors
// set a custom border thickness for all new cells created by the builder,
// then build a second row.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### See Also

* class [InternableComplexAttr](../internablecomplexattr/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
