---
title: Shading.BackgroundPatternColor
linktitle: BackgroundPatternColor
articleTitle: BackgroundPatternColor
second_title: Aspose.Words for .NET
description: Discover the Shading BackgroundPatternColor property to customize your Shading object's background color, enhancing your design's visual appeal.
type: docs
weight: 10
url: /net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Gets or sets the color that's applied to the background of the [`Shading`](../) object.

```csharp
public Color BackgroundPatternColor { get; set; }
```

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

### See Also

* class [Shading](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
