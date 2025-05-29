---
title: ThemeFonts Class
linktitle: ThemeFonts
articleTitle: ThemeFonts
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words ThemeFonts-klassen, ett kraftfullt verktyg för att hantera flerspråkiga teckensnittsscheman, vilket förbättrar dokumentets stil och läsbarhet.
type: docs
weight: 7350
url: /sv/net/aspose.words.themes/themefonts/
---
## ThemeFonts class

Representerar en samling teckensnitt i teckensnittsschemat, vilket gör det möjligt att ange olika teckensnitt för olika språk[`Latin`](./latin/) ,[`EastAsian`](./eastasian/) och[`ComplexScript`](./complexscript/) .

För att lära dig mer, besök[Arbeta med stilar och teman](https://docs.aspose.com/words/net/working-with-styles-and-themes/) dokumentationsartikel.

```csharp
public class ThemeFonts
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ComplexScript](../../aspose.words.themes/themefonts/complexscript/) { get; set; } | Anger teckensnittsnamn för ComplexScript-tecken. |
| [EastAsian](../../aspose.words.themes/themefonts/eastasian/) { get; set; } | Anger teckensnittsnamn för östasiatiska tecken. |
| [Latin](../../aspose.words.themes/themefonts/latin/) { get; set; } | Anger teckensnittsnamn för latinska tecken. |

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
