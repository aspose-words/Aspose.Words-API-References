---
title: Class ThemeColors
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Themes.ThemeColors klas. Stellt das Farbschema des Dokumentdesigns dar das zwölf Farben enthält.
type: docs
weight: 6480
url: /de/net/aspose.words.themes/themecolors/
---
## ThemeColors class

Stellt das Farbschema des Dokumentdesigns dar, das zwölf Farben enthält.

`ThemeColors` Das Objekt enthält sechs Akzentfarben, zwei dunkle Farben, zwei helle Farben und jeweils eine Farbe für einen Hyperlink und einen gefolgten Hyperlink.

```csharp
public class ThemeColors
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Gibt den Farbakzent 1 an. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Gibt den Farbakzent 2 an. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Gibt den Farbakzent 3 an. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Gibt den Farbakzent an. 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Gibt den Farbakzent an. 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Gibt den Farbakzent an. 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Gibt die Farbe Dunkel an. 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Gibt die Farbe Dunkel an. 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Gibt die Farbe für einen angeklickten Hyperlink an. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Gibt die Farbe für einen Hyperlink an. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Gibt die Farbe Licht an 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Gibt die Farbe Licht an. 2. |

### Beispiele

Zeigt, wie Sie benutzerdefinierte Farben und Schriftarten für Designs festlegen.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// Das „Theme“-Objekt gibt uns Zugriff auf das Dokumentthema, eine Quelle für Standardschriftarten und -farben.
Theme theme = doc.Theme;

// Einige Stile wie „Überschrift 1“ und „Untertitel“ erben diese Schriftarten.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Andere Sprachen haben möglicherweise auch ihre benutzerdefinierten Schriftarten in diesem Thema.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// Die Eigenschaft „Colors“ enthält die Farbpalette aus Microsoft Word,
// was erscheint, wenn die Schattierung oder die Schriftfarbe geändert wird.
// Wenden Sie benutzerdefinierte Farben auf die Farbpalette an, damit wir in Microsoft Word problemlos darauf zugreifen können
// wenn wir zum Beispiel über „Home“ -> die Schriftfarbe ändern "Schriftart" -> "Schriftfarbe",
// oder eine Form einfügen und dann über „Formformat“ eine Farbe dafür festlegen -> „Formstile“.
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

// Benutzerdefinierte Farben auf Hyperlinks im angeklickten und nicht angeklickten Zustand anwenden.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Themes](../../aspose.words.themes/)
* Montage [Aspose.Words](../../)


