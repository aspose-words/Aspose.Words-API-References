---
title: Shading.Texture
linktitle: Texture
articleTitle: Texture
second_title: Aspose.Words for .NET
description: Discover the Shading Texture property to enhance your designs. Easily customize and set textures for stunning visual effects in your projects.
type: docs
weight: 70
url: /net/aspose.words/shading/texture/
---
## Shading.Texture property

Gets or sets the shading texture.

```csharp
public TextureIndex Texture { get; set; }
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

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
