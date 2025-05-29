---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „DefaultFontSubstitution“ die Schrifteinstellungen für eine nahtlose Typografie optimiert. Verbessern Sie Ihr Design mit effektiven Regeln zur Schriftartersetzung.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Einstellungen im Zusammenhang mit der Standardregel zur Schriftartersetzung.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

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

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
