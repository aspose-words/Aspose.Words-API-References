---
title: Document.Theme
linktitle: Theme
articleTitle: Theme
second_title: Aspose.Words för .NET
description: Få tillgång till egenskapen Dokumenttema för att enkelt hämta temaobjektet, vilket förbättrar dokumentets design och visuella attraktionskraft.
type: docs
weight: 440
url: /sv/net/aspose.words/document/theme/
---
## Document.Theme property

Hämtar`Theme` objekt för detta dokument.

```csharp
public Theme Theme { get; }
```

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

* class [Theme](../../../aspose.words.themes/theme/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
