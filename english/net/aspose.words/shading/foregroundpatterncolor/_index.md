---
title: Shading.ForegroundPatternColor
linktitle: ForegroundPatternColor
second_title: Aspose.Words for .NET API Reference
description: Shading property. Gets or sets the color thats applied to the foreground of the Shading object in C#.
type: docs
weight: 40
url: /net/aspose.words/shading/foregroundpatterncolor/
---
## Shading.ForegroundPatternColor property

Gets or sets the color that's applied to the foreground of the [`Shading`](../) object.

```csharp
public Color ForegroundPatternColor { get; set; }
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
* namespace [Aspose.Words](../../shading/)
* assembly [Aspose.Words](../../../)
