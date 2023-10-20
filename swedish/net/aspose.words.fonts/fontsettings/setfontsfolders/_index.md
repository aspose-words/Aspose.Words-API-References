---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words för .NET
description: FontSettings SetFontsFolders metod. Ställer in mapparna där Aspose.Words söker efter TrueTypeteckensnitt vid rendering av dokument eller inbäddning av teckensnitt i C#.
type: docs
weight: 90
url: /sv/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Ställer in mapparna där Aspose.Words söker efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontsFolders | String[] | En uppsättning mappar som innehåller TrueType-teckensnitt. |
| recursive | Boolean | True för att skanna de angivna mapparna efter teckensnitt rekursivt. |

## Anmärkningar

Som standard letar Aspose.Words efter teckensnitt som är installerade i systemet.

Om du ställer in den här egenskapen återställs cachen för alla tidigare inlästa teckensnitt.

## Exempel

Visar hur du ställer in flera teckensnittskataloger.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Våra teckensnittskällor innehåller inte det teckensnitt som vi har använt för text i detta dokument.
// Om vi använder dessa teckensnittsinställningar när vi renderar detta dokument,
// Aspose.Words kommer att tillämpa ett reservteckensnitt på text som har ett teckensnitt som Aspose.Words inte kan hitta.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardteckensnittskällorna saknar de två typsnitten som vi använder i det här dokumentet.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Använd metoden "SetFontsFolders" för att skapa en teckensnittskälla från varje teckensnittskatalog som vi skickar som det första argumentet.
// Skicka "false" som det "rekursiva" argumentet för att inkludera teckensnitt från alla teckensnittsfiler som finns i katalogerna
// att vi skickar i det första argumentet, men inte inkluderar några typsnitt från någon av katalogernas undermappar.
// Ange "true" som det "rekursiva" argumentet för att inkludera alla teckensnittsfiler i katalogerna som vi skickar
// i det första argumentet, såväl som alla teckensnitt i deras underkataloger.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Själva mappen "Junction" innehåller inga teckensnittsfiler, men har undermappar som gör det.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Återställ de ursprungliga teckensnittskällorna.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Se även

* class [FontSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
