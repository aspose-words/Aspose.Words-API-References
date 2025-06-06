---
title: Shading.Texture
linktitle: Texture
articleTitle: Texture
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Skuggningstextur för att förbättra dina designer. Anpassa och ställ enkelt in texturer för fantastiska visuella effekter i dina projekt.
type: docs
weight: 70
url: /sv/net/aspose.words/shading/texture/
---
## Shading.Texture property

Hämtar eller ställer in skuggningstexturen.

```csharp
public TextureIndex Texture { get; set; }
```

## Exempel

Visar hur man dekorerar text med ramar och skuggning.

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

### Se även

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
