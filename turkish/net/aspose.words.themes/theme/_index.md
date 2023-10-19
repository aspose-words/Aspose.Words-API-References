---
title: Theme Class
linktitle: Theme
articleTitle: Theme
second_title: Aspose.Words for .NET
description: Aspose.Words.Themes.Theme sınıf. Belge Temasını temsil eder ve aşağıdakiler dahil ana tema parçalarına erişim sağlarMajorFonts MinorFonts VeColors C#'da.
type: docs
weight: 6460
url: /tr/net/aspose.words.themes/theme/
---
## Theme class

Belge Temasını temsil eder ve aşağıdakiler dahil ana tema parçalarına erişim sağlar:[`MajorFonts`](./majorfonts/) ,[`MinorFonts`](./minorfonts/) Ve[`Colors`](./colors/)

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Stiller ve Temalarla Çalışmak](https://docs.aspose.com/words/net/working-with-styles-and-themes/) dokümantasyon makalesi.

```csharp
public class Theme
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Theme](theme/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Colors](../../aspose.words.themes/theme/colors/) { get; } | Belge için tema renkleri kümesini belirlemeye olanak tanır. |
| [MajorFonts](../../aspose.words.themes/theme/majorfonts/) { get; } | Farklı diller için ana yazı tiplerini belirlemeye olanak tanır. |
| [MinorFonts](../../aspose.words.themes/theme/minorfonts/) { get; } | Farklı diller için ikincil yazı tipleri kümesini belirlemeye olanak tanır. |

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

* ad alanı [Aspose.Words.Themes](../../aspose.words.themes/)
* toplantı [Aspose.Words](../../)
