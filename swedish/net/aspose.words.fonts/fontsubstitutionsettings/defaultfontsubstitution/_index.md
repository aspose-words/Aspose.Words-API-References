---
title: DefaultFontSubstitution
second_title: Aspose.Words för .NET API Referens
description: Inställningar relaterade till standardregel för teckensnittsersättning.
type: docs
weight: 10
url: /sv/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Inställningar relaterade till standardregel för teckensnittsersättning.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

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

### Se även

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule)
* class [FontSubstitutionSettings](../../fontsubstitutionsettings)
* namnutrymme [Aspose.Words.Fonts](../../fontsubstitutionsettings)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->