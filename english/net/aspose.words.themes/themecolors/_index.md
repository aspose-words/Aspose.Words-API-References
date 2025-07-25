---
title: ThemeColors Class
linktitle: ThemeColors
articleTitle: ThemeColors
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.ThemeColors class, featuring a versatile 12-color scheme to enhance your document's visual appeal and consistency.
type: docs
weight: 7330
url: /net/aspose.words.themes/themecolors/
---
## ThemeColors class

Represents the color scheme of the document theme which contains twelve colors.

`ThemeColors` object contains six accent colors, two dark colors, two light colors and a color for each of a hyperlink and followed hyperlink.

```csharp
public class ThemeColors
```

## Properties

| Name | Description |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Specifies color Accent 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Specifies color Accent 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Specifies color Accent 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Specifies color Accent 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Specifies color Accent 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Specifies color Accent 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Specifies color Dark 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Specifies color Dark 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Specifies color for a clicked hyperlink. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Specifies color for a hyperlink. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Specifies color Light 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Specifies color Light 2. |

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

* namespace [Aspose.Words.Themes](../../aspose.words.themes/)
* assembly [Aspose.Words](../../)
