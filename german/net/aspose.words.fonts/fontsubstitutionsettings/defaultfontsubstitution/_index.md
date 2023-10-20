---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words für .NET
description: FontSubstitutionSettings DefaultFontSubstitution eigendom. Einstellungen im Zusammenhang mit der Standardregel zum Ersetzen von Schriftarten in C#.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Einstellungen im Zusammenhang mit der Standardregel zum Ersetzen von Schriftarten.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

## Beispiele

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

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
