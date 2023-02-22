---
title: Class DefaultFontSubstitutionRule
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule klas. Standardschriftersetzungsregel.
type: docs
weight: 2660
url: /de/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Standardschriftersetzungsregel.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Ruft den Namen der Standardschriftart ab oder legt ihn fest. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Gibt an, ob die Regel aktiviert ist oder nicht. |

### Bemerkungen

Diese Regel definiert einen einzigen Standardschriftnamen, der als Ersatz verwendet wird, wenn die ursprüngliche Schriftart nicht verfügbar ist.

### Beispiele

Zeigt, wie die Standardschriftersetzungsregel festgelegt wird.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Holen Sie sich die Standard-Ersetzungsregel in FontSettings.
// Diese Regel ersetzt alle fehlenden Schriftarten durch "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Stellen Sie den Ersatz für die Standardschriftart auf "Courier New" ein.
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Fügen Sie mit einem Document Builder Text in einer Schriftart hinzu, die wir nicht sehen müssen, damit die Ersetzung stattfindet,
// und dann das Ergebnis in ein PDF rendern.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Siehe auch

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


