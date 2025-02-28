---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words for .NET
description: Discover the ParagraphFormat Shading property for enhanced text styling. Access a Shading object to elevate your paragraph's visual appeal effortlessly.
type: docs
weight: 290
url: /net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Returns a [`Shading`](../../shading/) object that refers to the shading formatting for the paragraph.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
