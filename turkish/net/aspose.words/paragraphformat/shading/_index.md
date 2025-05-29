---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: .NET için Aspose.Words
description: Gelişmiş metin stili için ParagraphFormat Shading özelliğini keşfedin. Paragrafınızın görsel çekiciliğini zahmetsizce artırmak için bir Shading nesnesine erişin.
type: docs
weight: 290
url: /tr/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Bir[`Shading`](../../shading/) paragrafın gölgelendirme biçimlendirmesine başvuran nesne.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
