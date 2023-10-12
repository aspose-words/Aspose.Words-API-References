---
title: Class DefaultFontSubstitutionRule
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule klas. Standardregel zum Ersetzen von Schriftarten.
type: docs
weight: 2840
url: /de/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Standardregel zum Ersetzen von Schriftarten.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Ruft den Standardschriftnamen ab oder legt ihn fest. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Gibt an, ob die Regel aktiviert ist oder nicht. |

### Bemerkungen

Diese Regel definiert einen einzelnen Standardschriftartnamen, der als Ersatz verwendet wird, wenn die Originalschriftart nicht verfügbar ist.

### Beispiele

Zeigt, wie die Standardregel zum Ersetzen von Schriftarten festgelegt wird.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Die Standardersetzungsregel in FontSettings abrufen.
// Diese Regel ersetzt alle fehlenden Schriftarten durch „Times New Roman“.
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Setzen Sie den Standardschriftersatz auf „Courier New“.
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Fügen Sie mithilfe eines Dokumenterstellungsprogramms Text in einer Schriftart hinzu, die wir nicht benötigen, damit die Ersetzung stattfindet.
// und dann das Ergebnis in einem PDF rendern.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Siehe auch

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


