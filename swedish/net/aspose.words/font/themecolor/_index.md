---
title: Font.ThemeColor
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen Font ThemeColor för att förbättra dina designer med anpassningsbara temafärger i ditt färgschema.
type: docs
weight: 470
url: /sv/net/aspose.words/font/themecolor/
---
## Font.ThemeColor property

Hämtar eller ställer in temafärgen i det tillämpade färgschemat som är associerat med detta[`Font`](../) objekt.

```csharp
public ThemeColor ThemeColor { get; set; }
```

## Exempel

Visar hur man skapar och använder temainriktad stil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Skapa lite stil med temats teckensnittsegenskaper.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

Visar hur man arbetar med temateckensnitt och färger.

```csharp
Document doc = new Document();

// Definiera teckensnitt för språk som används som standard.
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

// 2 - Genom att ange namn på teckensnitt/färger som inte är temarelaterade:
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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
