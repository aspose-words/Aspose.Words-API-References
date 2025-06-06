---
title: Shading.BackgroundPatternColor
linktitle: BackgroundPatternColor
articleTitle: BackgroundPatternColor
second_title: .NET için Aspose.Words
description: Tasarımınızın görsel çekiciliğini artırmak için Shading nesnenizin arka plan rengini özelleştirmek üzere Shading BackgroundPatternColor özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Arka plana uygulanan rengi alır veya ayarlar[`Shading`](../) nesne.

```csharp
public Color BackgroundPatternColor { get; set; }
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
