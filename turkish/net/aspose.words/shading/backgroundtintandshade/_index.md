---
title: Shading.BackgroundTintAndShade
second_title: Aspose.Words for .NET API Referansı
description: Shading mülk. Arka plan tema rengini açan veya koyulaştıran çift değeri alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words/shading/backgroundtintandshade/
---
## Shading.BackgroundTintAndShade property

Arka plan tema rengini açan veya koyulaştıran çift değeri alır veya ayarlar.

```csharp
public double BackgroundTintAndShade { get; set; }
```

### Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ila 1 (en açık) aralığındadır. Sıfır (0) nötrdür. Bu özelliği -1'den küçük veya 1 'den büyük bir değere ayarlamaya çalışmak şu sonuçlarla sonuçlanır:ArgumentOutOfRangeException.

Bu özelliğin tema dışı renkler ile Gölgelendirme nesnesi için ayarlanması şu sonucu doğurur:InvalidOperationException.

### Örnekler

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
* ad alanı [Aspose.Words](../../shading/)
* toplantı [Aspose.Words](../../../)


