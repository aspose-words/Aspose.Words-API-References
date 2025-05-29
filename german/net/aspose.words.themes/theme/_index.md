---
title: Theme Class
linktitle: Theme
articleTitle: Theme
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Theme, um Ihre Dokumente mit anpassbaren Designs zu verbessern, darunter MajorFonts, MinorFonts und leuchtende Farben.
type: docs
weight: 7310
url: /de/net/aspose.words.themes/theme/
---
## Theme class

Stellt das Dokumentdesign dar und bietet Zugriff auf die wichtigsten Designteile, einschließlich[`MajorFonts`](./majorfonts/) ,[`MinorFonts`](./minorfonts/) Und[`Colors`](./colors/)

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Stilen und Designs](https://docs.aspose.com/words/net/working-with-styles-and-themes/) Dokumentationsartikel.

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
| [Colors](../../aspose.words.themes/theme/colors/) { get; } | Ermöglicht die Angabe der Designfarben für das Dokument. |
| [MajorFonts](../../aspose.words.themes/theme/majorfonts/) { get; } | Ermöglicht die Angabe der wichtigsten Schriftarten für verschiedene Sprachen. |
| [MinorFonts](../../aspose.words.themes/theme/minorfonts/) { get; } | Ermöglicht die Angabe des Satzes kleinerer Schriftarten für verschiedene Sprachen. |

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
