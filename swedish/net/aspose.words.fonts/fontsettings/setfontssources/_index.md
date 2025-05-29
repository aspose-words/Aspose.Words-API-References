---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words för .NET
description: Upptäck hur metoden SetFontsSources i Aspose.Words förbättrar dokumentrendering genom att ange TrueType-teckensnittskällor för optimala resultat.
type: docs
weight: 100
url: /sv/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Anger källorna där Aspose.Words letar efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sources | FontSourceBase[] | En matris med källor som innehåller TrueType-teckensnitt. |

## Anmärkningar

Som standard söker Aspose.Words efter teckensnitt som är installerade i systemet.

Om den här egenskapen ställs in återställs cachen för alla tidigare inlästa teckensnitt.

## Exempel

Visar hur man lägger till en teckensnittskälla till våra befintliga teckensnittskällor.

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

// Standardfontkällan saknar två av de fonter som vi använder i vårt dokument.
// När vi sparar det här dokumentet kommer Aspose.Words att använda reservteckensnitt på all text som är formaterad med oåtkomliga teckensnitt.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Skapa en typsnittskälla från en mapp som innehåller typsnitt.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Använd en ny array med teckensnittskällor som innehåller de ursprungliga teckensnittskällorna, såväl som våra anpassade teckensnitt.
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
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Anger källorna där Aspose.Words söker efter TrueType-teckensnitt och dessutom laddar tidigare sparad cache för teckensnittssökning.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sources | FontSourceBase[] | En matris med källor som innehåller TrueType-teckensnitt. |
| cacheInputStream | Stream | Indataström med sparad cache för teckensnittssökning. |

## Anmärkningar

Att ladda tidigare sparad cache för teckensnittssökning påskyndar initialiseringsprocessen för teckensnittscachen. Det är särskilt användbart när åtkomst till teckensnittskällor är komplicerad (t.ex. när teckensnitt laddas via nätverk).

När du sparar och laddar cachen för teckensnittssökning identifieras teckensnitt i de angivna källorna via cachenyckeln. För teckensnitten i[`SystemFontSource`](../../systemfontsource/) och[`FolderFontSource`](../../folderfontsource/) Cache-nyckeln är sökvägen till typsnittsfilen. För[`MemoryFontSource`](../../memoryfontsource/) och[`StreamFontSource`](../../streamfontsource/)cachenyckeln är definierad i[`CacheKey`](../../memoryfontsource/cachekey/) och[`CacheKey`](../../streamfontsource/cachekey/) properties respektive. För[`FileFontSource`](../../filefontsource/) cachenyckeln är antingen[`CacheKey`](../../filefontsource/cachekey/) egenskapen eller en filsökväg om[`CacheKey`](../../filefontsource/cachekey/) är`null`.

Det rekommenderas starkt att använda samma teckensnittskällor när cachen laddas som när cachen sparades. Eventuella ändringar i teckensnittskällorna (t.ex. lägga till nya teckensnitt, flytta teckensnittsfiler eller ändra cachenyckeln) kan leda till att Aspose.Words inte tolkar teckensnittet korrekt.

## Exempel

Visar hur man påskyndar initialiseringsprocessen för teckensnittscachen.

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
/// Ladda endast teckensnittsdata när det behövs istället för att lagra dem i minnet
/// för hela livslängden för "FontSettings"-objektet.
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
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
