---
title: ThemeFonts Class
linktitle: ThemeFonts
articleTitle: ThemeFonts
second_title: Aspose.Words for .NET
description: Aspose.Words.Themes.ThemeFonts class. Represents a collection of fonts in the font scheme allowing to specify different fonts for different languages Latin EastAsian and ComplexScript in C#.
type: docs
weight: 6640
url: /net/aspose.words.themes/themefonts/
---
## ThemeFonts class

Represents a collection of fonts in the font scheme, allowing to specify different fonts for different languages [`Latin`](./latin/), [`EastAsian`](./eastasian/) and [`ComplexScript`](./complexscript/).

To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/net/working-with-styles-and-themes/) documentation article.

```csharp
public class ThemeFonts
```

## Properties

| Name | Description |
| --- | --- |
| [ComplexScript](../../aspose.words.themes/themefonts/complexscript/) { get; set; } | Specifies font name for ComplexScript characters. |
| [EastAsian](../../aspose.words.themes/themefonts/eastasian/) { get; set; } | Specifies font name for EastAsian characters. |
| [Latin](../../aspose.words.themes/themefonts/latin/) { get; set; } | Specifies font name for Latin characters. |

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
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

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

* namespace [Aspose.Words.Themes](../../aspose.words.themes/)
* assembly [Aspose.Words](../../)
