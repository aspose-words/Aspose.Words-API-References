---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words for .NET
description: Shading ForegroundTintAndShade mülk. Ön plan tema rengini açan veya koyulaştıran bir çift değer alır veya ayarlar C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Ön plan tema rengini açan veya koyulaştıran bir çift değer alır veya ayarlar.

```csharp
public double ForegroundTintAndShade { get; set; }
```

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ila 1 (en açık) aralığındadır. Sıfır (0) nötrdür. Bu özelliği -1'den küçük veya 1 'den büyük bir değere ayarlamaya çalışmak şu sonuçlarla sonuçlanır:ArgumentOutOfRangeException.

Bu özelliğin tema dışı renkler ile Gölgelendirme nesnesi için ayarlanması şu sonucu doğurur:InvalidOperationException.

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
