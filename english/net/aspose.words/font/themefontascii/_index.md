---
title: Font.ThemeFontAscii
linktitle: ThemeFontAscii
articleTitle: ThemeFontAscii
second_title: Aspose.Words for .NET
description: Discover the Font ThemeFontAscii property to easily customize theme fonts for Latin text (codes 0-127) in your design, enhancing visual appeal.
type: docs
weight: 490
url: /net/aspose.words/font/themefontascii/
---
## Font.ThemeFontAscii property

Gets or sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [`Font`](../) object.

```csharp
public ThemeFont ThemeFontAscii { get; set; }
```

## Examples

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

* enum [ThemeFont](../../../aspose.words.themes/themefont/)
* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
