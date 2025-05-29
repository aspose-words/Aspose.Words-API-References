---
title: ThemeColors.Dark2
linktitle: Dark2
articleTitle: Dark2
second_title: .NET için Aspose.Words
description: ThemeColors Dark2'yi keşfedin. Çarpıcı görseller ve büyüleyici bir kullanıcı deneyimi için zengin bir Dark 2 rengiyle tasarımınızı kolayca oluşturun.
type: docs
weight: 80
url: /tr/net/aspose.words.themes/themecolors/dark2/
---
## ThemeColors.Dark2 property

Koyu rengi belirtir 2.

```csharp
public Color Dark2 { get; set; }
```

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

* class [ThemeColors](../)
* ad alanı [Aspose.Words.Themes](../../../aspose.words.themes/)
* toplantı [Aspose.Words](../../../)
