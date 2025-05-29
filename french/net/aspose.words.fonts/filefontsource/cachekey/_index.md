---
title: FileFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FileFontSource CacheKey, votre clé pour une gestion efficace des polices et une mise en cache optimisée pour des performances améliorées.
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/filefontsource/cachekey/
---
## FileFontSource.CacheKey property

La clé de cette source dans le cache.

```csharp
public string CacheKey { get; }
```

## Remarques

Cette clé est utilisée pour identifier l'élément du cache lors de l'enregistrement/chargement du cache de recherche de polices avec [`SaveSearchCache`](../../fontsettings/savesearchcache/) et [`SetFontsSources`](../../fontsettings/setfontssources/) méthodes.

Si la clé n'est pas spécifiée, alors[`FilePath`](../filepath/) sera utilisé comme clé à la place.

## Exemples

Montre comment accélérer le processus d’initialisation du cache de polices.

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
/// Chargez les données de police uniquement lorsque cela est nécessaire au lieu de les stocker dans la mémoire
/// pendant toute la durée de vie de l'objet « FontSettings ».
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

### Voir également

* class [FileFontSource](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
