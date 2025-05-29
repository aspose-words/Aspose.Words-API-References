---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words för .NET
description: Upptäck hur du enkelt kan anpassa dokumentteckensnittsinställningar. Förbättra dina dokument med skräddarsydda teckensnittsalternativ för förbättrad läsbarhet och stil.
type: docs
weight: 150
url: /sv/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Hämtar eller ställer in dokumentets teckensnittsinställningar.

```csharp
public FontSettings FontSettings { get; set; }
```

## Anmärkningar

Den här egenskapen gör det möjligt att ange teckensnittsinställningar per dokument. Om den är inställd på`null` , standardinställningar för statiskt teckensnitt [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) kommer att användas.

Standardvärdet är`null`.

## Exempel

Visar hur man ställer in regler för teckensnittsersättning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Standardfontkällorna innehåller det första font som dokumentet använder.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Det andra typsnittet, "Amethysta", är inte tillgängligt.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Vi kan konfigurera en tabell för typsnittsersättning som bestämmer
// vilka typsnitt Aspose.Words kommer att använda som ersättning för otillgängliga typsnitt.
// Ställ in två ersättningsfonter för "Amethysta": "Arvo" och "Courier New".
// Om den första ersättningen inte är tillgänglig försöker Aspose.Words använda den andra ersättningen, och så vidare.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" är inte tillgängligt, och substitutionsregeln anger att det första teckensnittet som ska användas som ersättning är "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" är inte heller tillgängligt, men det är "Courier New".
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Utdatadokumentet visar texten som använder teckensnittet "Amethysta" formaterat med "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Se även

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
