---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode SetFontsSources dans Aspose.Words améliore le rendu des documents en spécifiant les sources de polices TrueType pour des résultats optimaux.
type: docs
weight: 100
url: /fr/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Définit les sources où Aspose.Words recherche les polices TrueType lors du rendu de documents ou de l'incorporation de polices.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sources | FontSourceBase[] | Un tableau de sources contenant des polices TrueType. |

## Remarques

Par défaut, Aspose.Words recherche les polices installées sur le système.

La définition de cette propriété réinitialise le cache de toutes les polices précédemment chargées.

## Exemples

Montre comment ajouter une source de police à nos sources de polices existantes.

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

// La source de police par défaut manque de deux des polices que nous utilisons dans notre document.
// Lorsque nous enregistrons ce document, Aspose.Words appliquera des polices de secours à tout texte formaté avec des polices inaccessibles.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Créez une source de police à partir d'un dossier contenant des polices.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Appliquez un nouveau tableau de sources de polices contenant les sources de polices d'origine, ainsi que nos polices personnalisées.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Vérifiez qu'Aspose.Words a accès à toutes les polices requises avant de rendre le document au format PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Restaurer les sources de polices d'origine.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Voir également

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Définit les sources où Aspose.Words recherche les polices TrueType et charge en plus le cache de recherche de polices précédemment enregistré .

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sources | FontSourceBase[] | Un tableau de sources contenant des polices TrueType. |
| cacheInputStream | Stream | Flux d'entrée avec cache de recherche de polices enregistré. |

## Remarques

Charger le cache de recherche de polices précédemment enregistré accélère le processus d'initialisation du cache. Ceci est particulièrement utile lorsque l'accès aux sources de polices est complexe (par exemple, lorsque les polices sont chargées via le réseau).

Lors de l'enregistrement et du chargement du cache de recherche de polices, les polices des sources fournies sont identifiées via la clé de cache. Pour les polices du[`SystemFontSource`](../../systemfontsource/) et[`FolderFontSource`](../../folderfontsource/) La clé de cache est le chemin d'accès au fichier de police. Pour[`MemoryFontSource`](../../memoryfontsource/) et[`StreamFontSource`](../../streamfontsource/)la clé de cache est définie dans le[`CacheKey`](../../memoryfontsource/cachekey/) et[`CacheKey`](../../streamfontsource/cachekey/) properties respectivement. Pour le[`FileFontSource`](../../filefontsource/) la clé de cache est soit[`CacheKey`](../../filefontsource/cachekey/) propriété ou un chemin de fichier si le[`CacheKey`](../../filefontsource/cachekey/) est`nul`.

Il est fortement recommandé de fournir les mêmes sources de polices lors du chargement du cache qu'au moment de l'enregistrement du cache. Toute modification des sources de polices (par exemple, l'ajout de nouvelles polices, le déplacement de fichiers de polices ou la modification de la clé de cache) peut entraîner une résolution de police inexacte par Aspose.Words.

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

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
