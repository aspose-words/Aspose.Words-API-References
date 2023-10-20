---
title: Theme Class
linktitle: Theme
articleTitle: Theme
second_title: Aspose.Words für .NET
description: Aspose.Words.Themes.Theme klas. Stellt das Dokumentthema dar und bietet Zugriff auf die Hauptthementeile einschließlichMajorFonts MinorFonts UndColors in C#.
type: docs
weight: 6460
url: /de/net/aspose.words.themes/theme/
---
## Theme class

Stellt das Dokumentthema dar und bietet Zugriff auf die Hauptthementeile, einschließlich[`MajorFonts`](./majorfonts/) ,[`MinorFonts`](./minorfonts/) Und[`Colors`](./colors/)

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Stilen und Themen](https://docs.aspose.com/words/net/working-with-styles-and-themes/) Dokumentationsartikel.

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
| [Colors](../../aspose.words.themes/theme/colors/) { get; } | Ermöglicht die Angabe der Themenfarben für das Dokument. |
| [MajorFonts](../../aspose.words.themes/theme/majorfonts/) { get; } | Ermöglicht die Angabe des Satzes wichtiger Schriftarten für verschiedene Sprachen. |
| [MinorFonts](../../aspose.words.themes/theme/minorfonts/) { get; } | Ermöglicht die Angabe des Satzes kleinerer Schriftarten für verschiedene Sprachen. |

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

* namensraum [Aspose.Words.Themes](../../aspose.words.themes/)
* Montage [Aspose.Words](../../)
