---
title: ThemeFonts.EastAsian
linktitle: EastAsian
articleTitle: EastAsian
second_title: Aspose.Words for .NET
description: Discover ThemeFonts' EastAsian property to easily customize font names for enhanced readability of East Asian characters. Elevate your design today!
type: docs
weight: 20
url: /net/aspose.words.themes/themefonts/eastasian/
---
## ThemeFonts.EastAsian property

Specifies font name for EastAsian characters.

```csharp
public string EastAsian { get; set; }
```

## Examples

Shows how to set custom colors and fonts for themes.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// The "Theme" object gives us access to the document theme, a source of default fonts and colors.
Theme theme = doc.Theme;

// Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Other languages may also have their custom fonts in this theme.
Assert.That(theme.MajorFonts.ComplexScript, Is.EqualTo(string.Empty));
Assert.That(theme.MajorFonts.EastAsian, Is.EqualTo(string.Empty));
Assert.That(theme.MinorFonts.ComplexScript, Is.EqualTo(string.Empty));
Assert.That(theme.MinorFonts.EastAsian, Is.EqualTo(string.Empty));

// The "Colors" property contains the color palette from Microsoft Word,
// which appears when changing shading or font color.
// Apply custom colors to the color palette so we have easy access to them in Microsoft Word
// when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
// or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
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

// Apply custom colors to hyperlinks in their clicked and un-clicked states.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### See Also

* class [ThemeFonts](../)
* namespace [Aspose.Words.Themes](../../../aspose.words.themes/)
* assembly [Aspose.Words](../../../)
