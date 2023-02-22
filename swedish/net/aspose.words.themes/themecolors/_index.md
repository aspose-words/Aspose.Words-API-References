---
title: Class ThemeColors
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Themes.ThemeColors klass. Representerar färgschemat för dokumenttemat som innehåller tolv färger.
type: docs
weight: 6180
url: /sv/net/aspose.words.themes/themecolors/
---
## ThemeColors class

Representerar färgschemat för dokumenttemat som innehåller tolv färger.

ThemeColors-objektet innehåller sex accentfärger, två mörka färger, två ljusa färger och en färg för var och en av en hyperlänk och följt hyperlänk.

```csharp
public class ThemeColors
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Anger färg Accent 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Anger färg Accent 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Anger färg Accent 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Anger färg Accent 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Anger färg Accent 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Anger färg Accent 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Anger färg Dark 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Anger färg Dark 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Anger färg för en klickad hyperlänk. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Anger färg för en hyperlänk. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Anger färg Ljus 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Anger färg Ljus 2. |

### Exempel

Visar hur du ställer in anpassade färger och teckensnitt för teman.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// "Theme"-objektet ger oss tillgång till dokumenttemat, en källa till standardteckensnitt och färger.
Theme theme = doc.Theme;

// Vissa stilar, som "Rubrik 1" och "Underrubrik", kommer att ärva dessa typsnitt.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Andra språk kan också ha sina anpassade typsnitt i detta tema.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// Egenskapen "Colors" innehåller färgpaletten från Microsoft Word,
// som visas när du ändrar skuggning eller teckensnittsfärg.
// Använd anpassade färger på färgpaletten så att vi har enkel tillgång till dem i Microsoft Word
// när vi till exempel ändrar teckensnittsfärg via "Hem" -> "Teckensnitt" -> "Fontfärg",
// eller infoga en form och ställ sedan in en färg för den via "Shape Format" -> "Formstilar".
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

// Tillämpa anpassade färger på hyperlänkar i deras klickade och oklickade tillstånd.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Se även

* namnutrymme [Aspose.Words.Themes](../../aspose.words.themes/)
* hopsättning [Aspose.Words](../../)


