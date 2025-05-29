---
title: Shading.BackgroundPatternThemeColor
linktitle: BackgroundPatternThemeColor
articleTitle: BackgroundPatternThemeColor
second_title: .NET için Aspose.Words
description: Tasarımınızı benzersiz arka plan desenleri ve renk şemalarıyla geliştirmek için Shading BackgroundPatternThemeColor özelliğini nasıl özelleştireceğinizi keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/shading/backgroundpatternthemecolor/
---
## Shading.BackgroundPatternThemeColor property

Bu renk şemasıyla ilişkili uygulanan renk şemasındaki arka plan desen teması rengini alır veya ayarlar[`Shading`](../) nesne.

```csharp
public ThemeColor BackgroundPatternThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
