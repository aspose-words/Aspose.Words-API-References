---
title: StreamFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words pour .NET
description: Découvrez la propriété StreamFontSource CacheKey, optimisez votre gestion des polices avec une mise en cache efficace pour des temps de chargement plus rapides et des performances améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/streamfontsource/cachekey/
---
## StreamFontSource.CacheKey property

La clé de cette source dans le cache.

```csharp
public string CacheKey { get; }
```

## Remarques

Cette clé est utilisée pour identifier l'élément de cache lors de l'enregistrement/chargement du cache de recherche de polices avec [`SaveSearchCache`](../../fontsettings/savesearchcache/) et[`SetFontsSources`](../../fontsettings/setfontssources/) méthodes.

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

* class [StreamFontSource](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
