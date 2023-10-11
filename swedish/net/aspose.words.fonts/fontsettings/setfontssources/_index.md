---
title: FontSettings.SetFontsSources
second_title: Aspose.Words för .NET API Referens
description: FontSettings metod. Ställer in källorna där Aspose.Words söker efter TrueTypeteckensnitt vid rendering av dokument eller inbäddning av teckensnitt.
type: docs
weight: 100
url: /sv/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(FontSourceBase[]) {#setfontssources}

Ställer in källorna där Aspose.Words söker efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sources | FontSourceBase[] | En mängd källor som innehåller TrueType-teckensnitt. |

### Anmärkningar

Som standard letar Aspose.Words efter teckensnitt som är installerade i systemet.

Om du ställer in den här egenskapen återställs cachen för alla tidigare inlästa teckensnitt.

### Exempel

Visar hur du lägger till en teckensnittskälla till våra befintliga teckensnittskällor.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardfontkällan saknar två av de teckensnitt som vi använder i vårt dokument.
// När vi sparar det här dokumentet kommer Aspose.Words att tillämpa reservteckensnitt på all text som är formaterad med otillgängliga teckensnitt.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Skapa en teckensnittskälla från en mapp som innehåller teckensnitt.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Använd en ny uppsättning teckensnittskällor som innehåller de ursprungliga teckensnittskällorna, såväl som våra anpassade teckensnitt.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verifiera att Aspose.Words har tillgång till alla nödvändiga teckensnitt innan vi renderar dokumentet till PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Återställ de ursprungliga teckensnittskällorna.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Se även

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../fontsettings/)
* hopsättning [Aspose.Words](../../../)

---

## SetFontsSources(FontSourceBase[], Stream) {#setfontssources_1}

Ställer in källorna där Aspose.Words söker efter TrueType-teckensnitt och laddar dessutom tidigare sparad typsnittssökningscache.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sources | FontSourceBase[] | En mängd källor som innehåller TrueType-teckensnitt. |
| cacheInputStream | Stream | Indataström med sparad typsnittssökningscache. |

### Anmärkningar

Om du laddar tidigare sparad typsnittssökningscache påskyndar initieringsprocessen för typsnittscache. Det är särskilt användbart när åtkomst till teckensnittskällor är komplicerad (t.ex. när teckensnitt laddas via nätverk).

När du sparar och laddar typsnittssökningscache identifieras typsnitt i de angivna källorna via cache-nyckel. För typsnitten i[`SystemFontSource`](../../systemfontsource/) och[`FolderFontSource`](../../folderfontsource/) cache-nyckeln är sökvägen till teckensnittsfilen. För[`MemoryFontSource`](../../memoryfontsource/) och[`StreamFontSource`](../../streamfontsource/) cache-nyckeln är definierad i[`CacheKey`](../../memoryfontsource/cachekey/) och[`CacheKey`](../../streamfontsource/cachekey/) egenskaper respektive. För[`FileFontSource`](../../filefontsource/) cache-nyckeln är antingen[`CacheKey`](../../filefontsource/cachekey/) egenskap eller en filsökväg om[`CacheKey`](../../filefontsource/cachekey/) är`null`.

Det rekommenderas starkt att du tillhandahåller samma teckensnittskällor när du laddar cacheminnet som när cachen sparades. Alla ändringar i teckensnittskällorna (t.ex. att lägga till nya teckensnitt, flytta teckensnittsfiler eller ändra cache-nyckeln) kan leda till att teckensnittet blir felaktigt lösas av Aspose.Words.

### Exempel

Visar hur man snabbar upp initieringsprocessen för teckensnittscache.

```csharp
public void LoadFontSearchCache()
{
    const string cacheKey1 = "Arvo";
    const string cacheKey2 = "Arvo-Bold";
    FontSettings parsedFonts = new FontSettings();
    FontSettings loadedCache = new FontSettings();

    parsedFonts.SetFontsSources(new FontSourceBase[]
    {
        new FileFontSource(FontsDir + "Arvo-Regular.ttf", 0, cacheKey1),
        new FileFontSource(FontsDir + "Arvo-Bold.ttf", 0, cacheKey2)
    });

    using (MemoryStream cacheStream = new MemoryStream())
    {
        parsedFonts.SaveSearchCache(cacheStream);
        loadedCache.SetFontsSources(new FontSourceBase[]
        {
            new SearchCacheStream(cacheKey1),                    
            new MemoryFontSource(File.ReadAllBytes(FontsDir + "Arvo-Bold.ttf"), 0, cacheKey2)
        }, cacheStream);
    }

    Assert.AreEqual(parsedFonts.GetFontsSources().Length, loadedCache.GetFontsSources().Length);
}

/// <summary>
/// Ladda teckensnittsdata endast när det behövs istället för att lagra det i minnet
/// under hela livslängden för objektet "FontSettings".
/// </summary>
private class SearchCacheStream : StreamFontSource
{
    public SearchCacheStream(string cacheKey):base(0, cacheKey)
    {
    }

    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Arvo-Regular.ttf");
    }
}
```

### Se även

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../fontsettings/)
* hopsättning [Aspose.Words](../../../)


