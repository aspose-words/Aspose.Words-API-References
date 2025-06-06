---
title: ThemeColors Class
linktitle: ThemeColors
articleTitle: ThemeColors
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.ThemeColors mit einem vielseitigen 12-Farben-Schema zur Verbesserung der visuellen Attraktivität und Konsistenz Ihres Dokuments.
type: docs
weight: 7330
url: /de/net/aspose.words.themes/themecolors/
---
## ThemeColors class

Stellt das Farbschema des Dokumentdesigns dar, das zwölf Farben enthält.

`ThemeColors` Das Objekt enthält sechs Akzentfarben, zwei dunkle Farben, zwei helle Farben und jeweils eine Farbe für einen Hyperlink und einen verfolgten Hyperlink.

```csharp
public class ThemeColors
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Gibt die Farbe Akzent 1 an. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Gibt die Farbe Akzent 2 an. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Gibt den Farbakzent 3 an. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Gibt den Farbakzent 4 an. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Gibt den Farbakzent 5 an. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Gibt den Farbakzent 6 an. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Gibt die Farbe Dunkel 1 an. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Gibt die Farbe Dunkel 2 an. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Gibt die Farbe für einen angeklickten Hyperlink an. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Gibt die Farbe für einen Hyperlink an. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Gibt die Farbe Licht 1 an. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Gibt die Farbe Licht 2 an. |

## Beispiele

Zeigt, wie benutzerdefinierte Farben und Schriftarten für Designs festgelegt werden.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// Das Objekt „Design“ gibt uns Zugriff auf das Dokumentdesign, eine Quelle für Standardschriftarten und -farben.
Theme theme = doc.Theme;

// Einige Stile, wie „Überschrift 1“ und „Untertitel“, übernehmen diese Schriftarten.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Auch andere Sprachen können in diesem Design über eigene Schriftarten verfügen.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// Die Eigenschaft „Farben“ enthält die Farbpalette von Microsoft Word,
// das beim Ändern der Schattierung oder Schriftfarbe erscheint.
// Wenden Sie benutzerdefinierte Farben auf die Farbpalette an, damit wir in Microsoft Word einfach darauf zugreifen können
// wenn wir beispielsweise über "Home" -> "Schriftart" -> "Schriftfarbe" die Schriftfarbe ändern,
// oder fügen Sie eine Form ein und legen Sie dann über „Formformat“ -> „Formstile“ eine Farbe dafür fest.
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

// Wenden Sie benutzerdefinierte Farben auf Hyperlinks im angeklickten und nicht angeklickten Zustand an.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Themes](../../aspose.words.themes/)
* Montage [Aspose.Words](../../)
