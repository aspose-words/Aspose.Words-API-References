---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.DefaultFontSubstitutionRule för sömlös typsnittshantering och förbättrad dokumentformatering. Optimera ditt arbetsflöde idag!
type: docs
weight: 3250
url: /sv/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Standardregel för teckensnittsersättning.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Hämtar eller ställer in standardnamnet på teckensnittet. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Anger om regeln är aktiverad eller inte. |

## Anmärkningar

Denna regel definierar ett enda standardtypsnitt som ska användas för ersättning om det ursprungliga typsnittet inte är tillgängligt.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
