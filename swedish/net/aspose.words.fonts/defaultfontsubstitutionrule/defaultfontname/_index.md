---
title: DefaultFontSubstitutionRule.DefaultFontName
linktitle: DefaultFontName
articleTitle: DefaultFontName
second_title: Aspose.Words för .NET
description: Upptäck hur du enkelt hanterar DefaultFontSubstitutionRule och anpassar ditt standardteckensnittsnamn för ökad designflexibilitet.
type: docs
weight: 10
url: /sv/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Hämtar eller ställer in standardnamnet på teckensnittet.

```csharp
public string DefaultFontName { get; set; }
```

## Anmärkningar

Standardvärdet är 'Times New Roman'.

## Exempel

Visar hur man ställer in standardregeln för teckensnittsersättning.

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

// Ställ in standardteckensnittsersättningen till "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Använd en dokumentbyggare, lägg till text i ett teckensnitt som vi inte behöver se för att substitutionen ska ske,
// och sedan rendera resultatet i en PDF.
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

// Typsnittskällorna som dokumentet använder innehåller typsnittet "Arial", men inte "Arvo".
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Ställ in egenskapen "DefaultFontName" till "Courier New" för att,
// när dokumentet renderas, använd det teckensnittet i alla fall när ett annat teckensnitt inte är tillgängligt.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words kommer nu att använda standardteckensnittet istället för eventuella saknade teckensnitt under renderingsanrop.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Se även

* class [DefaultFontSubstitutionRule](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
