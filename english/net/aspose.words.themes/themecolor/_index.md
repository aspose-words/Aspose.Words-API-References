---
title: ThemeColor Enum
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words ThemeColor enum for customizing document themes with vibrant colors, enhancing your document's visual appeal and professionalism.
type: docs
weight: 7390
url: /net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

Specifies the theme colors for document themes.

To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/net/working-with-styles-and-themes/) documentation article.

```csharp
public enum ThemeColor
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `-1` | No color. |
| Dark1 | `0` | Dark main color 1. |
| Light1 | `1` | Light main color 1. |
| Dark2 | `2` | Dark main color 2. |
| Light2 | `3` | Light main color 2. |
| Accent1 | `4` | Accent color 1. |
| Accent2 | `5` | Accent color 2. |
| Accent3 | `6` | Accent color 3. |
| Accent4 | `7` | Accent color 4. |
| Accent5 | `8` | Accent color 5. |
| Accent6 | `9` | Accent color 6. |
| Hyperlink | `10` | Hyperlink color. |
| FollowedHyperlink | `11` | Followed hyperlink color. |
| Text1 | `12` | Text color 1. |
| Text2 | `13` | Text color 2. |
| Background1 | `14` | Background color 1. |
| Background2 | `15` | Background color 2. |

## Remarks

The specified theme color is a reference to one of the predefined theme colors, located in the document's Theme part, which allows color information to be set centrally in the document.

## Examples

Shows how to create and use themed style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Create some style with theme font properties.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

Shows how to work with theme fonts and colors.

```csharp
Document doc = new Document();

// Define fonts for languages uses by default.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// We can use theme font and color instead of default values.
font.ThemeFont = ThemeFont.Minor;
font.ThemeColor = ThemeColor.Accent2;

Assert.That(font.ThemeFont, Is.EqualTo(ThemeFont.Minor));
Assert.That(font.Name, Is.EqualTo("Algerian"));

Assert.That(font.ThemeFontAscii, Is.EqualTo(ThemeFont.Minor));
Assert.That(font.NameAscii, Is.EqualTo("Algerian"));

Assert.That(font.ThemeFontBi, Is.EqualTo(ThemeFont.Minor));
Assert.That(font.NameBi, Is.EqualTo("Andalus"));

Assert.That(font.ThemeFontFarEast, Is.EqualTo(ThemeFont.Minor));
Assert.That(font.NameFarEast, Is.EqualTo("Aharoni"));

Assert.That(font.ThemeFontOther, Is.EqualTo(ThemeFont.Minor));
Assert.That(font.NameOther, Is.EqualTo("Algerian"));

Assert.That(font.ThemeColor, Is.EqualTo(ThemeColor.Accent2));
Assert.That(font.Color, Is.EqualTo(Color.Empty));

// There are several ways of reset them font and color.
// 1 -  By setting ThemeFont.None/ThemeColor.None:
font.ThemeFont = ThemeFont.None;
font.ThemeColor = ThemeColor.None;

Assert.That(font.ThemeFont, Is.EqualTo(ThemeFont.None));
Assert.That(font.Name, Is.EqualTo("Algerian"));

Assert.That(font.ThemeFontAscii, Is.EqualTo(ThemeFont.None));
Assert.That(font.NameAscii, Is.EqualTo("Algerian"));

Assert.That(font.ThemeFontBi, Is.EqualTo(ThemeFont.None));
Assert.That(font.NameBi, Is.EqualTo("Andalus"));

Assert.That(font.ThemeFontFarEast, Is.EqualTo(ThemeFont.None));
Assert.That(font.NameFarEast, Is.EqualTo("Aharoni"));

Assert.That(font.ThemeFontOther, Is.EqualTo(ThemeFont.None));
Assert.That(font.NameOther, Is.EqualTo("Algerian"));

Assert.That(font.ThemeColor, Is.EqualTo(ThemeColor.None));
Assert.That(font.Color, Is.EqualTo(Color.Empty));

// 2 -  By setting non-theme font/color names:
font.Name = "Arial";
font.Color = Color.Blue;

Assert.That(font.ThemeFont, Is.EqualTo(ThemeFont.None));
Assert.That(font.Name, Is.EqualTo("Arial"));

Assert.That(font.ThemeFontAscii, Is.EqualTo(ThemeFont.None));
Assert.That(font.NameAscii, Is.EqualTo("Arial"));

Assert.That(font.ThemeFontBi, Is.EqualTo(ThemeFont.None));
Assert.That(font.NameBi, Is.EqualTo("Arial"));

Assert.That(font.ThemeFontFarEast, Is.EqualTo(ThemeFont.None));
Assert.That(font.NameFarEast, Is.EqualTo("Arial"));

Assert.That(font.ThemeFontOther, Is.EqualTo(ThemeFont.None));
Assert.That(font.NameOther, Is.EqualTo("Arial"));

Assert.That(font.ThemeColor, Is.EqualTo(ThemeColor.None));
Assert.That(font.Color.ToArgb(), Is.EqualTo(Color.Blue.ToArgb()));
```

### See Also

* namespace [Aspose.Words.Themes](../../aspose.words.themes/)
* assembly [Aspose.Words](../../)
