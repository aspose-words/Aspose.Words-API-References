---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words för .NET
description: Upptäck hur du använder SetFontsFolders-metoden i Aspose.Words för att anpassa TrueType-teckensnittsplaceringar för optimal dokumentrendering och inbäddning.
type: docs
weight: 90
url: /sv/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Anger mapparna där Aspose.Words letar efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontsFolders | String[] | En matris med mappar som innehåller TrueType-teckensnitt. |
| recursive | Boolean | Sant för att söka igenom de angivna mapparna rekursivt efter teckensnitt. |

## Anmärkningar

Som standard söker Aspose.Words efter teckensnitt som är installerade i systemet.

Om den här egenskapen ställs in återställs cachen för alla tidigare inlästa teckensnitt.

## Exempel

Visar hur man ställer in flera källkataloger för teckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Våra typsnittskällor innehåller inte det typsnitt som vi har använt för texten i det här dokumentet.
// Om vi använder dessa teckensnittsinställningar när vi renderar detta dokument,
// Aspose.Words kommer att använda ett reservteckensnitt för text som har ett teckensnitt som Aspose.Words inte kan hitta.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardfontkällorna saknar de två fonter som vi använder i det här dokumentet.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Använd metoden "SetFontsFolders" för att skapa en teckensnittskälla från varje teckensnittskatalog som vi skickar som första argument.
// Skicka "false" som argumentet "rekursivt" för att inkludera teckensnitt från alla teckensnittsfiler som finns i katalogerna
// som vi skickar med i det första argumentet, men inte inkluderar några teckensnitt från någon av katalogernas undermappar.
// Skicka "true" som argumentet "rekursivt" för att inkludera alla teckensnittsfiler i de kataloger vi skickar
// i det första argumentet, såväl som alla teckensnitt i deras underkataloger.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Själva mappen "Junction" innehåller inga typsnittsfiler, men har undermappar som gör det.
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
