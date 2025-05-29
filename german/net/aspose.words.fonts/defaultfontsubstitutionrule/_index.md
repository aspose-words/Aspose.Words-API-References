---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.DefaultFontSubstitutionRule für nahtloses Schriftmanagement und verbesserte Dokumentformatierung. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 3250
url: /de/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Standardregel zur Schriftartersetzung.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Ruft den Standardschriftnamen ab oder legt ihn fest. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Gibt an, ob die Regel aktiviert ist oder nicht. |

## Bemerkungen

Diese Regel definiert einen einzelnen Standardschriftnamen, der als Ersatz verwendet wird, wenn die Originalschrift nicht verfügbar ist.

## Beispiele

Zeigt, wie die Standardregel zur Schriftartersetzung festgelegt wird.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Holen Sie sich die Standard-Ersetzungsregel innerhalb von FontSettings.
// Diese Regel ersetzt alle fehlenden Schriftarten durch „Times New Roman“.
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Legen Sie den Standardschriftersatz auf „Courier New“ fest.
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Fügen Sie mithilfe eines Dokumentgenerators Text in einer Schriftart hinzu, die wir nicht benötigen, damit die Ersetzung sichtbar wird.
// und rendern Sie dann das Ergebnis in einem PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Siehe auch

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
