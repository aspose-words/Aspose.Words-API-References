---
title: Theme.Colors
second_title: Aspose.Words für .NET-API-Referenz
description: Theme eigendom. Ermöglicht das Festlegen des Satzes von Designfarben für das Dokument.
type: docs
weight: 20
url: /de/net/aspose.words.themes/theme/colors/
---
## Theme.Colors property

Ermöglicht das Festlegen des Satzes von Designfarben für das Dokument.

```csharp
public ThemeColors Colors { get; }
```

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

* class [ThemeColors](../../themecolors/)
* class [Theme](../)
* namensraum [Aspose.Words.Themes](../../theme/)
* Montage [Aspose.Words](../../../)


