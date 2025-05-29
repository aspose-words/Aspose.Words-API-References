---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: Aspose.Words för .NET
description: Upptäck hur du använder SetFontsFolder-metoden för att ange en TrueType-teckensnittskatalog i Aspose.Words, vilket förbättrar dokumentrendering och teckensnittsinbäddning.
type: docs
weight: 80
url: /sv/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Anger mappen där Aspose.Words letar efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt. Detta är en genväg till[`SetFontsFolders`](../setfontsfolders/) för att endast ställa in en typsnittskatalog.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontFolder | String | Mappen som innehåller TrueType-teckensnitt. |
| recursive | Boolean | Sant för att söka igenom de angivna mapparna rekursivt efter teckensnitt. |

## Exempel

Visar hur man ställer in en källkatalog för teckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Våra typsnittskällor innehåller inte det typsnitt som vi har använt för texten i det här dokumentet.
// Om vi använder dessa teckensnittsinställningar när vi renderar detta dokument,
// Aspose.Words kommer att använda ett reservteckensnitt för text som har ett teckensnitt som Aspose.Words inte kan hitta.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardfontkällorna saknar de två fonter som vi använder i det här dokumentet.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Använd metoden "SetFontsFolder" för att ange en katalog som ska fungera som en ny teckensnittskälla.
// Skicka "false" som argumentet "rekursivt" för att inkludera teckensnitt från alla teckensnittsfiler som finns i katalogen
// som vi skickar med i det första argumentet, men inte inkluderar några teckensnitt i någon av undermapparna i den katalogen.
// Skicka "true" som argumentet "rekursivt" för att inkludera alla teckensnittsfiler i den katalog vi skickar
// i det första argumentet, såväl som alla teckensnitt i dess underkataloger.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Typsnittet "Amethysta" finns i en undermapp i typsnittskatalogen.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Återställ de ursprungliga teckensnittskällorna.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Se även

* class [FontSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
