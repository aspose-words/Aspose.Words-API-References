---
title: ThemeColor Enum
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words ThemeColor-Aufzählung zum Anpassen von Dokumentthemen mit lebendigen Farben und verbessern Sie so die visuelle Attraktivität und Professionalität Ihres Dokuments.
type: docs
weight: 7320
url: /de/net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

Gibt die Designfarben für Dokumentdesigns an.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Stilen und Designs](https://docs.aspose.com/words/net/working-with-styles-and-themes/) Dokumentationsartikel.

```csharp
public enum ThemeColor
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `-1` | Keine Farbe. |
| Dark1 | `0` | Dunkle Hauptfarbe 1. |
| Light1 | `1` | Helle Hauptfarbe 1. |
| Dark2 | `2` | Dunkle Hauptfarbe 2. |
| Light2 | `3` | Helle Hauptfarbe 2. |
| Accent1 | `4` | Akzentfarbe 1. |
| Accent2 | `5` | Akzentfarbe 2. |
| Accent3 | `6` | Akzentfarbe 3. |
| Accent4 | `7` | Akzentfarbe 4. |
| Accent5 | `8` | Akzentfarbe 5. |
| Accent6 | `9` | Akzentfarbe 6. |
| Hyperlink | `10` | Hyperlinkfarbe. |
| FollowedHyperlink | `11` | Farbe des verfolgten Hyperlinks. |
| Text1 | `12` | Textfarbe 1. |
| Text2 | `13` | Textfarbe 2. |
| Background1 | `14` | Hintergrundfarbe 1. |
| Background2 | `15` | Hintergrundfarbe 2. |

## Bemerkungen

Die angegebene Designfarbe ist ein Verweis auf eine der vordefinierten Designfarben, die sich im Designteil des Dokuments befinden und die zentrale Festlegung von Farbinformationen im Dokument ermöglichen.

## Beispiele

Zeigt, wie man einen Themenstil erstellt und verwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Erstellen Sie einen Stil mit den Schrifteigenschaften des Designs.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

Zeigt, wie mit Designschriftarten und -farben gearbeitet wird.

```csharp
Document doc = new Document();

// Definieren Sie Schriftarten für die standardmäßig verwendeten Sprachen.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// Wir können die Schriftart und Farbe des Designs anstelle der Standardwerte verwenden.
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

// Es gibt mehrere Möglichkeiten, Schriftart und Farbe zurückzusetzen.
// 1 – Durch Festlegen von ThemeFont.None/ThemeColor.None:
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

// 2 – Durch Festlegen von Schriftart-/Farbnamen, die nicht zum Design gehören:
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

### Siehe auch

* namensraum [Aspose.Words.Themes](../../aspose.words.themes/)
* Montage [Aspose.Words](../../)
