---
title: Enum ThemeColor
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Themes.ThemeColor uppräkning. Anger temafärgerna för dokumentteman.
type: docs
weight: 6470
url: /sv/net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

Anger temafärgerna för dokumentteman.

För att lära dig mer, besök[Arbeta med stilar och teman](https://docs.aspose.com/words/net/working-with-styles-and-themes/) dokumentationsartikel.

```csharp
public enum ThemeColor
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `-1` | Ingen färg. |
| Dark1 | `0` | Mörk huvudfärg 1. |
| Light1 | `1` | Ljus huvudfärg 1. |
| Dark2 | `2` | Mörk huvudfärg 2. |
| Light2 | `3` | Ljus huvudfärg 2. |
| Accent1 | `4` | Accentfärg 1. |
| Accent2 | `5` | Accentfärg 2. |
| Accent3 | `6` | Accentfärg 3. |
| Accent4 | `7` | Accentfärg 4. |
| Accent5 | `8` | Accentfärg 5. |
| Accent6 | `9` | Accentfärg 6. |
| Hyperlink | `10` | Hyperlänksfärg. |
| FollowedHyperlink | `11` | Följde hyperlänksfärg. |
| Text1 | `12` | Textfärg 1. |
| Text2 | `13` | Textfärg 2. |
| Background1 | `14` | Bakgrundsfärg 1. |
| Background2 | `15` | Bakgrundsfärg 2. |

### Anmärkningar

Den angivna temafärgen är en referens till en av de fördefinierade temafärgerna, som finns i dokumentets temadel, vilket gör att färginformation kan ställas in centralt i dokumentet.

### Exempel

Visar hur man skapar och använder stil med teman.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Skapa lite stil med egenskaper för tematypsnitt.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

Visar hur man arbetar med tematypsnitt och färger.

```csharp
Document doc = new Document();

// Definiera typsnitt för språk som används som standard.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// Vi kan använda tematypsnitt och färg istället för standardvärden.
font.ThemeFont = ThemeFont.Minor;
font.ThemeColor = ThemeColor.Accent2;

Assert.AreEqual(ThemeFont.Minor, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.Accent2, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// Det finns flera sätt att återställa teckensnitt och färg.
// 1 - Genom att ställa in ThemeFont.None/ThemeColor.None:
font.ThemeFont = ThemeFont.None;
font.ThemeColor = ThemeColor.None;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// 2 - Genom att ställa in teckensnitt/färgnamn som inte är tema:
font.Name = "Arial";
font.Color = Color.Blue;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Arial", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Arial", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Arial", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Arial", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Arial", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Blue.ToArgb(), font.Color.ToArgb());
```

### Se även

* namnutrymme [Aspose.Words.Themes](../../aspose.words.themes/)
* hopsättning [Aspose.Words](../../)


