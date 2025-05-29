---
title: Shading.ForegroundPatternColor
linktitle: ForegroundPatternColor
articleTitle: ForegroundPatternColor
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım ve görsel çekicilik için Gölgeleme nesnenizin ön plan rengini özelleştirmek üzere Gölgeleme Ön Plan Deseni Rengi özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words/shading/foregroundpatterncolor/
---
## Shading.ForegroundPatternColor property

Ön plana uygulanan rengi alır veya ayarlar[`Shading`](../) nesne.

```csharp
public Color ForegroundPatternColor { get; set; }
```

## Örnekler

Metnin kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

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

* class [Shading](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
