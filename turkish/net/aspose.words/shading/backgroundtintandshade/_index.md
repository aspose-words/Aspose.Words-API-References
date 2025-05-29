---
title: Shading.BackgroundTintAndShade
linktitle: BackgroundTintAndShade
articleTitle: BackgroundTintAndShade
second_title: .NET için Aspose.Words
description: BackgroundTintAndShade özelliğiyle arka plan temanızın rengini zahmetsizce ayarlayın. Mükemmel bir tasarım dokunuşu için renkleri açın veya koyulaştırın!
type: docs
weight: 30
url: /tr/net/aspose.words/shading/backgroundtintandshade/
---
## Shading.BackgroundTintAndShade property

Arka plan tema rengini açan veya koyulaştıran bir çift değer alır veya ayarlar.

```csharp
public double BackgroundTintAndShade { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Bu özelliği -1'den küçük veya 1'den büyük bir değere ayarlarsanız fırlatın. |
| InvalidOperationException | Bu özelliği Gölgeleme nesnesi için tema renkleri dışında bir renkle ayarlarsanız fırlatın. |

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ile 1 (en açık) arasında değişmektedir.

Sıfır (0) nötrdür.

## Örnekler

Gölgelendirme dokusu için ön plan ve arka plan renklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### Ayrıca bakınız

* class [Shading](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
