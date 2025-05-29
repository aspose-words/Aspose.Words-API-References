---
title: ThemeColors Class
linktitle: ThemeColors
articleTitle: ThemeColors
second_title: .NET için Aspose.Words
description: Belgenizin görsel çekiciliğini ve tutarlılığını artıracak çok yönlü 12 renk şemasına sahip Aspose.Words.ThemeColors sınıfını keşfedin.
type: docs
weight: 7330
url: /tr/net/aspose.words.themes/themecolors/
---
## ThemeColors class

On iki renkten oluşan belge temasının renk şemasını temsil eder.

`ThemeColors` nesne altı vurgu rengi, iki koyu renk, iki açık renk ve bir köprü metni ve takip edilen köprü metni için bir renk içerir.

```csharp
public class ThemeColors
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Renk Vurgusu 1'i belirtir. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Renk Vurgusu 2'yi belirtir. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Renk Vurgusu 3'ü belirtir. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Renk Vurgusu 4'ü belirtir. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Renk Vurgusu 5'i belirtir. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Renk Vurgusu 6'yı belirtir. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Koyu rengi belirtir 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Koyu rengi belirtir 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Tıklanan bir köprü metni için renk belirtir. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Bir köprü metni için renk belirtir. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Renk Işık 1'i belirtir. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Renk Işığını belirtir 2. |

## Örnekler

Temalar için özel renklerin ve yazı tiplerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// "Tema" nesnesi bize varsayılan yazı tipleri ve renklerin kaynağı olan belge temasına erişim sağlar.
Theme theme = doc.Theme;

// "Başlık 1" ve "Alt Başlık" gibi bazı stiller bu yazı tiplerini devralacaktır.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Bu temada diğer dillerin de kendilerine ait özel yazı tipleri olabilir.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// "Renkler" özelliği Microsoft Word'den renk paletini içerir.
// Gölgelendirme veya yazı rengi değiştirilirken görünen.
// Microsoft Word'de bunlara kolayca erişebilmemiz için renk paletine özel renkler uygulayın
// örneğin, "Ana Sayfa" -> "Yazı Tipi" -> "Yazı Tipi Rengi" yoluyla yazı tipi rengini değiştirdiğimizde,
// veya bir şekil ekleyin ve ardından "Şekil Biçimi" -> "Şekil Stilleri" yoluyla bunun için bir renk ayarlayın.
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

// Tıklanmış ve tıklanmamış durumlarındaki köprü metinlerine özel renkler uygulayın.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Themes](../../aspose.words.themes/)
* toplantı [Aspose.Words](../../)
