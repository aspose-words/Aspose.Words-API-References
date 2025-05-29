---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen DefaultFontSubstitution optimerar teckensnittsinställningarna för sömlös typografi. Förbättra din design med effektiva regler för teckensnittsersättning.
type: docs
weight: 10
url: /sv/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Inställningar relaterade till standardregeln för teckensnittsersättning.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

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

### Se även

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
