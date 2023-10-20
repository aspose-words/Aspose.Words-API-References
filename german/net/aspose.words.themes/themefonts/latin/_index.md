---
title: ThemeFonts.Latin
linktitle: Latin
articleTitle: Latin
second_title: Aspose.Words für .NET
description: ThemeFonts Latin eigendom. Gibt den Schriftartnamen für lateinische Zeichen an in C#.
type: docs
weight: 30
url: /de/net/aspose.words.themes/themefonts/latin/
---
## ThemeFonts.Latin property

Gibt den Schriftartnamen für lateinische Zeichen an.

```csharp
public string Latin { get; set; }
```

## Beispiele

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

* class [ThemeFonts](../)
* namensraum [Aspose.Words.Themes](../../../aspose.words.themes/)
* Montage [Aspose.Words](../../../)
