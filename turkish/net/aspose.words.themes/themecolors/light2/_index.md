---
title: ThemeColors.Light2
linktitle: Light2
articleTitle: Light2
second_title: Aspose.Words for .NET
description: ThemeColors Light2 mülk. Açık renk 2. yi belirtir C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.themes/themecolors/light2/
---
## ThemeColors.Light2 property

Açık renk 2. 'yi belirtir

```csharp
public Color Light2 { get; set; }
```

## Örnekler

Temalar için özel renklerin ve yazı tiplerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// "Tema" nesnesi, varsayılan yazı tipleri ve renklerin kaynağı olan belge temasına erişmemizi sağlar.
Theme theme = doc.Theme;

// "Başlık 1" ve "Altyazı" gibi bazı stiller bu yazı tiplerini devralır.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Bu temada diğer dillerin de kendi özel yazı tipleri olabilir.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// "Renkler" özelliği Microsoft Word'ün renk paletini içerir,
// gölgeleme veya yazı tipi rengini değiştirirken görünen.
// Renk paletine özel renkler uygulayın, böylece Microsoft Word'de bunlara kolayca erişebilelim
// örneğin yazı tipi rengini "Ana Sayfa" aracılığıyla değiştirdiğimizde -> "Yazı Tipi" -> "Yazı rengi",
// veya bir şekil ekleyin ve ardından "Şekil Formatı" aracılığıyla bunun için bir renk ayarlayın --> "Şekil Stilleri".
ThemeColors colors = theme.Colors;
colors.Dark1 = Color.MidnightBlue;
colors.Light1 = Color.PaleGreen;
colors.Dark2 = Color.Indigo;
colors.Light2 = Color.Khaki;

colors.Accent1 = Color.OrangeRed;
colors.Accent2 = Color.LightSalmon;
colors.Accent3 = Color.Yellow;
colors.Accent4 = Color.Gold;
colors.Accent5 = Color.BlueViolet;
colors.Accent6 = Color.DarkViolet;

// Köprülere tıklanmış ve tıklanmamış durumlarında özel renkler uygulayın.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Ayrıca bakınız

* class [ThemeColors](../)
* ad alanı [Aspose.Words.Themes](../../../aspose.words.themes/)
* toplantı [Aspose.Words](../../../)
