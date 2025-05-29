---
title: Shading.Texture
linktitle: Texture
articleTitle: Texture
second_title: .NET için Aspose.Words
description: Tasarımlarınızı geliştirmek için Gölgeleme Dokusu özelliğini keşfedin. Projelerinizde çarpıcı görsel efektler için dokuları kolayca özelleştirin ve ayarlayın.
type: docs
weight: 70
url: /tr/net/aspose.words/shading/texture/
---
## Shading.Texture property

Gölgelendirme dokusunu alır veya ayarlar.

```csharp
public TextureIndex Texture { get; set; }
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

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
