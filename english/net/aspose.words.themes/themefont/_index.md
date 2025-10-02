---
title: ThemeFont Enum
linktitle: ThemeFont
articleTitle: ThemeFont
second_title: Aspose.Words for .NET
description: Discover Aspose.Words ThemeFont enum to easily manage document theme fonts and enhance your documents' visual appeal with tailored styles.
type: docs
weight: 7400
url: /net/aspose.words.themes/themefont/
---
## ThemeFont enumeration

Specifies the types of theme font names for document themes.

```csharp
public enum ThemeFont
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No theme font. |
| Major | `1` | Major theme font. |
| Minor | `2` | Minor theme font. |

## Remarks

Specifies a theme font type which can be referenced as a theme font within the parent object properties. This theme font is a reference to one of the predefined theme fonts, located in the document's Theme part, which allows for font information to be set centrally in the document.

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
