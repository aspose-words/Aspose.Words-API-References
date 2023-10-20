---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words pour .NET
description: FontSettings SetFontsSources méthode. Définit les sources dans lesquelles Aspose.Words recherche les polices TrueType lors du rendu de documents ou de lintégration de polices en C#.
type: docs
weight: 100
url: /fr/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Définit les sources dans lesquelles Aspose.Words recherche les polices TrueType lors du rendu de documents ou de l'intégration de polices.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sources | FontSourceBase[] | Tableau de sources contenant des polices TrueType. |

## Remarques

Par défaut, Aspose.Words recherche les polices installées sur le système.

La définition de cette propriété réinitialise le cache de toutes les polices précédemment chargées.

## Exemples

Montre comment ajouter une source de polices à nos sources de polices existantes.

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

// Il manque deux des polices que nous utilisons dans notre document dans la source de police par défaut.
// Lorsque nous enregistrons ce document, Aspose.Words appliquera des polices de secours à tout le texte formaté avec des polices inaccessibles.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Crée une source de polices à partir d'un dossier contenant des polices.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Applique un nouveau tableau de sources de polices contenant les sources de polices d'origine, ainsi que nos polices personnalisées.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Vérifiez qu'Aspose.Words a accès à toutes les polices requises avant de rendre le document au format PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Restaure les sources de polices d'origine.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Voir également

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Définit les sources dans lesquelles Aspose.Words recherche les polices TrueType et charge en outre le cache de recherche de polices précédemment enregistré .

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sources | FontSourceBase[] | Tableau de sources contenant des polices TrueType. |
| cacheInputStream | Stream | Flux d’entrée avec cache de recherche de polices enregistré. |

## Remarques

Le chargement du cache de recherche de polices précédemment enregistré accélérera le processus d'initialisation du cache de polices. C'est particulièrement utile lorsque l'accès aux sources de polices est compliqué (par exemple lorsque les polices sont chargées via le réseau).

Lors de l'enregistrement et du chargement du cache de recherche de polices, les polices des sources fournies sont identifiées via la clé de cache. Pour les polices du[`SystemFontSource`](../../systemfontsource/) et[`FolderFontSource`](../../folderfontsource/) la clé de cache est le chemin vers le fichier de police. Pour[`MemoryFontSource`](../../memoryfontsource/) et[`StreamFontSource`](../../streamfontsource/) la clé de cache est définie dans le[`CacheKey`](../../memoryfontsource/cachekey/) et[`CacheKey`](../../streamfontsource/cachekey/) Properties respectivement. Pour le[`FileFontSource`](../../filefontsource/) la clé de cache est soit[`CacheKey`](../../filefontsource/cachekey/) propriété ou un chemin de fichier si le[`CacheKey`](../../filefontsource/cachekey/) est`nul`.

Il est fortement recommandé de fournir les mêmes sources de polices lors du chargement du cache qu'au moment où le cache a été enregistré. Toute modification des sources de polices (par exemple, ajout de nouvelles polices, déplacement de fichiers de polices ou modification de la clé de cache) peut conduire à une police inexacte . résolution par Aspose.Words.

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
/// Charge les données de police uniquement lorsque cela est nécessaire au lieu de les stocker dans la mémoire
/// pendant toute la durée de vie de l'objet "FontSettings".
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

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
