---
title: Class Theme
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Themes.Theme klas. Stellt das Dokumentdesign dar und bietet Zugriff auf Hauptdesignteile einschließlichMajorFonts MinorFonts undColors
type: docs
weight: 6160
url: /de/net/aspose.words.themes/theme/
---
## Theme class

Stellt das Dokumentdesign dar und bietet Zugriff auf Hauptdesignteile, einschließlich[`MajorFonts`](./majorfonts/) ,[`MinorFonts`](./minorfonts/) und[`Colors`](./colors/)

```csharp
public class Theme
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Theme](theme/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Colors](../../aspose.words.themes/theme/colors/) { get; } | Ermöglicht das Festlegen des Satzes von Designfarben für das Dokument. |
| [MajorFonts](../../aspose.words.themes/theme/majorfonts/) { get; } | Ermöglicht die Angabe der wichtigsten Schriftarten für verschiedene Sprachen. |
| [MinorFonts](../../aspose.words.themes/theme/minorfonts/) { get; } | Ermöglicht das Festlegen des Satzes von untergeordneten Schriftarten für verschiedene Sprachen. |

### Beispiele

Zeigt, wie benutzerdefinierte Farben und Schriftarten für Designs festgelegt werden.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// Das "Theme"-Objekt gibt uns Zugriff auf das Dokumentdesign, eine Quelle für Standardschriftarten und -farben.
Theme theme = doc.Theme;

// Einige Stile wie "Überschrift 1" und "Untertitel" erben diese Schriftarten.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Andere Sprachen haben möglicherweise auch ihre benutzerdefinierten Schriftarten in diesem Thema.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// Die Eigenschaft "Colors" enthält die Farbpalette von Microsoft Word,
// was erscheint, wenn die Schattierung oder Schriftfarbe geändert wird.
// Wenden Sie benutzerdefinierte Farben auf die Farbpalette an, damit wir in Microsoft Word einfachen Zugriff darauf haben
// wenn wir zum Beispiel die Schriftfarbe über "Home" -> "Schriftart" -> "Schriftfarbe",
// oder füge eine Form ein und setze dann eine Farbe dafür über "Shape Format" -> "Formstile".
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


