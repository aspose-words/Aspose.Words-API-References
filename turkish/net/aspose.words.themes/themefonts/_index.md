---
title: Class ThemeFonts
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Themes.ThemeFonts sınıf. Yazı tipi şemasındaki yazı tiplerinin bir koleksiyonunu temsil eder ve farklı diller için farklı yazı tipleri belirlemeye olanak tanırLatin EastAsian VeComplexScript .
type: docs
weight: 6500
url: /tr/net/aspose.words.themes/themefonts/
---
## ThemeFonts class

Yazı tipi şemasındaki yazı tiplerinin bir koleksiyonunu temsil eder ve farklı diller için farklı yazı tipleri belirlemeye olanak tanır[`Latin`](./latin/) ,[`EastAsian`](./eastasian/) Ve[`ComplexScript`](./complexscript/) .

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Stiller ve Temalarla Çalışmak](https://docs.aspose.com/words/net/working-with-styles-and-themes/) dokümantasyon makalesi.

```csharp
public class ThemeFonts
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ComplexScript](../../aspose.words.themes/themefonts/complexscript/) { get; set; } | ComplexScript karakterleri için yazı tipi adını belirtir. |
| [EastAsian](../../aspose.words.themes/themefonts/eastasian/) { get; set; } | DoğuAsya karakterleri için yazı tipi adını belirtir. |
| [Latin](../../aspose.words.themes/themefonts/latin/) { get; set; } | Latin karakterler için yazı tipi adını belirtir. |

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


