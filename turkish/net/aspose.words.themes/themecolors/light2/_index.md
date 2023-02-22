---
title: ThemeColors.Light2
second_title: Aspose.Words for .NET API Referansı
description: ThemeColors mülk. Açık 2. rengini belirtir
type: docs
weight: 120
url: /tr/net/aspose.words.themes/themecolors/light2/
---
## ThemeColors.Light2 property

Açık 2. rengini belirtir

```csharp
public Color Light2 { get; set; }
```

### Örnekler

Temalar için özel renklerin ve yazı tiplerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// "Tema" nesnesi, varsayılan yazı tiplerinin ve renklerin kaynağı olan belge temasına erişmemizi sağlar.
Theme theme = doc.Theme;

// "Heading 1" ve "Subtitle" gibi bazı stiller bu yazı tiplerini devralır.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Diğer diller de bu temada kendi özel yazı tiplerine sahip olabilir.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// "Renkler" özelliği, Microsoft Word'den renk paletini içerir,
// gölgelendirmeyi veya yazı tipi rengini değiştirirken görünen.
// Microsoft Word'de kolayca erişebilmemiz için renk paletine özel renkler uygulayın
// örneğin yazı tipi rengini "Ana Sayfa" ile değiştirdiğimizde -> "Yazı Tipi" -> "Yazı rengi",
// veya bir şekil ekleyin ve ardından "Şekil Formatı" ile bunun için bir renk ayarlayın -> "Şekil Stilleri".
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

// Tıklanan ve tıklanmayan durumlarındaki köprülere özel renkler uygulayın.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Ayrıca bakınız

* class [ThemeColors](../)
* ad alanı [Aspose.Words.Themes](../../themecolors/)
* toplantı [Aspose.Words](../../../)


