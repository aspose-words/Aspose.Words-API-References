---
title: DefaultFontSubstitutionRule.DefaultFontName
linktitle: DefaultFontName
articleTitle: DefaultFontName
second_title: Aspose.Words für .NET
description: DefaultFontSubstitutionRule DefaultFontName eigendom. Ruft den Standardschriftnamen ab oder legt ihn fest in C#.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Ruft den Standardschriftnamen ab oder legt ihn fest.

```csharp
public string DefaultFontName { get; set; }
```

## Bemerkungen

Der Standardwert ist „Times New Roman“.

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

Zeigt, wie eine Standardschriftart angegeben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Die Schriftartquellen, die das Dokument verwendet, enthalten die Schriftart „Arial“, aber nicht „Arvo“.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Setzen Sie die Eigenschaft „DefaultFontName“ auf „Courier New“,
 // Beim Rendern des Dokuments diese Schriftart in allen Fällen anwenden, in denen keine andere Schriftart verfügbar ist.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words verwendet jetzt bei allen Rendering-Aufrufen die Standardschriftart anstelle aller fehlenden Schriftarten.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Siehe auch

* class [DefaultFontSubstitutionRule](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
