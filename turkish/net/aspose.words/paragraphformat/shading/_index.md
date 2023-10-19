---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words for .NET
description: ParagraphFormat Shading mülk. Bir değeri döndürürShading paragrafın gölgelendirme formatını ifade eden nesne C#'da.
type: docs
weight: 280
url: /tr/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Bir değeri döndürür[`Shading`](../../shading/) paragrafın gölgelendirme formatını ifade eden nesne.

```csharp
public Shading Shading { get; }
```

## Örnekler

Metnin kenarlıklar ve gölgelendirmeyle nasıl süsleneceğini gösterir.

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

### Ayrıca bakınız

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
