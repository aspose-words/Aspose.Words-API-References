---
title: DefaultFontSubstitutionRule.DefaultFontName
second_title: Aspose.Words för .NET API Referens
description: DefaultFontSubstitutionRule fast egendom. Hämtar eller ställer in standardteckensnittsnamnet.
type: docs
weight: 10
url: /sv/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Hämtar eller ställer in standardteckensnittsnamnet.

```csharp
public string DefaultFontName { get; set; }
```

### Anmärkningar

Standardvärdet är 'Times New Roman'.

### Exempel

Visar hur du ställer in standardregeln för teckensnittsersättning.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Hämta standardsubstitutionsregeln i FontSettings.
// Denna regel kommer att ersätta alla saknade teckensnitt med "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Ställ in standardtypsnittsersättningen till "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Med hjälp av en dokumentbyggare, lägg till lite text i ett teckensnitt som vi inte behöver se ersättningen ske,
// och rendera sedan resultatet i en PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

Visar hur man anger ett standardteckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Teckensnittskällorna som dokumentet använder innehåller typsnittet "Arial", men inte "Arvo".
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Ställ in egenskapen "DefaultFontName" till "Courier New" till,
 // medan du renderar dokumentet, använd det teckensnittet i alla fall när ett annat teckensnitt inte är tillgängligt.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words kommer nu att använda standardteckensnittet i stället för eventuella saknade teckensnitt under alla renderingsanrop.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Se även

* class [DefaultFontSubstitutionRule](../)
* namnutrymme [Aspose.Words.Fonts](../../defaultfontsubstitutionrule/)
* hopsättning [Aspose.Words](../../../)


