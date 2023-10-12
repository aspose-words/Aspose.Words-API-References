---
title: Class ThemeColors
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Themes.ThemeColors sınıf. On iki renk içeren belge temasının renk düzenini temsil eder.
type: docs
weight: 6480
url: /tr/net/aspose.words.themes/themecolors/
---
## ThemeColors class

On iki renk içeren belge temasının renk düzenini temsil eder.

`ThemeColors` nesne altı vurgu rengi, iki koyu renk, iki açık renk ve her köprü ve takip edilen köprü için bir renk içerir.

```csharp
public class ThemeColors
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Renk Vurgusunu belirtir 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Renk Vurgusunu belirtir 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Renk Vurgusunu belirtir 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Renk Vurgusunu belirtir 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Renk Vurgusunu belirtir 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Renk Vurgusunu belirtir 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Rengi belirtir Koyu 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Rengi belirtir Koyu 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Tıklanan köprünün rengini belirtir. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Köprünün rengini belirtir. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Açık renk 1. 'yi belirtir |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Açık renk 2. 'yi belirtir |

### Örnekler

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

* ad alanı [Aspose.Words.Themes](../../aspose.words.themes/)
* toplantı [Aspose.Words](../../)


