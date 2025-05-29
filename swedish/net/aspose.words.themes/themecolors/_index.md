---
title: ThemeColors Class
linktitle: ThemeColors
articleTitle: ThemeColors
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ThemeColors, med ett mångsidigt schema med 12 färger som förbättrar ditt dokuments visuella attraktionskraft och konsekvens.
type: docs
weight: 7330
url: /sv/net/aspose.words.themes/themecolors/
---
## ThemeColors class

Representerar färgschemat för dokumenttemat som innehåller tolv färger.

`ThemeColors` Objektet innehåller sex accentfärger, två mörka färger, två ljusa färger och en färg för var och en av en hyperlänk och en efterföljande hyperlänk.

```csharp
public class ThemeColors
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Anger färgaccent 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Anger färgaccent 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Anger färgaccent 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Anger färgaccent 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Anger färgaccent 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Anger färgaccent 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Anger färg Mörk 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Anger färg Mörk 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Anger färg för en klickad hyperlänk. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Anger färg för en hyperlänk. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Anger färg Ljus 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Anger färg Ljus 2. |

## Exempel

Visar hur man ställer in anpassade färger och teckensnitt för teman.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// Objektet "Tema" ger oss tillgång till dokumenttemat, en källa till standardteckensnitt och färger.
Theme theme = doc.Theme;

// Vissa stilar, som "Rubrik 1" och "Undertext", ärver dessa teckensnitt.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Andra språk kan också ha sina egna teckensnitt i detta tema.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// Egenskapen "Färger" innehåller färgpaletten från Microsoft Word,
// som visas när man ändrar skuggning eller teckenfärg.
// Använd anpassade färger på färgpaletten så att vi har enkel åtkomst till dem i Microsoft Word
// när vi till exempel ändrar teckenfärgen via "Hem" -> "Teckensnitt" -> "Teckenfärg",
// eller infoga en form och ange sedan en färg för den via "Formformat" -> "Formstilar".
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

// Använd anpassade färger på hyperlänkar i deras klickade och oklickade tillstånd.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Se även

* namnutrymme [Aspose.Words.Themes](../../aspose.words.themes/)
* hopsättning [Aspose.Words](../../)
