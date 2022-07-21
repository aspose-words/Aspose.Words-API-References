---
title: FontSettings
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie les paramètres de police pour un document.
type: docs
weight: 2790
url: /fr/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Spécifie les paramètres de police pour un document.

```csharp
public class FontSettings
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FontSettings](fontsettings)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance) { get; } | Paramètres de police par défaut statiques. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings) { get; } | Paramètres liés au mécanisme de remplacement des polices. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings) { get; } | Paramètres liés au mécanisme de substitution de polices. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources)() | Obtient une copie du tableau qui contient la liste des sources où Aspose.Words recherche les polices TrueType. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources)() | Réinitialise les sources de polices aux valeurs par défaut du système. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache)(Stream) | Enregistre le cache de recherche de polices dans le flux. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder)(string, bool) | Définit le dossier dans lequel Aspose.Words recherche les polices TrueType lors du rendu de documents ou de l'intégration de polices. Il s'agit d'un raccourci vers[`SetFontsFolders`](./setfontsfolders) pour définir un seul répertoire de polices. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders)(string[], bool) | Définit les dossiers dans lesquels Aspose.Words recherche les polices TrueType lors du rendu de documents ou de l'intégration de polices. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources#setfontssources)(FontSourceBase[]) | Définit les sources où Aspose.Words recherche les polices TrueType lors du rendu de documents ou de l'intégration de polices. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources#setfontssources_1)(FontSourceBase[], Stream) | Définit les sources où Aspose.Words recherche les polices TrueType et charge en outre le cache de recherche de polices précédemment enregistré . |

### Remarques

Aspose.Words utilise les paramètres de police pour résoudre les polices dans le document. Les polices sont principalement résolues lors de la création du document layout ou du rendu dans des formats de page fixes. Mais lors du chargement de certains formats, Aspose.Words peut également nécessiter de résoudre les polices. Par exemple, lorsque chargement de documents HTML, Aspose.Words peut résoudre les polices pour effectuer un remplacement des polices. Il est donc recommandé de définir les paramètres de police in [`LoadOptions`](../../aspose.words.loading/loadoptions) lors du chargement du document. Ou du moins avant de créer la mise en page ou de rendre le document au format page fixe.

Par défaut, tous les documents utilisent une seule instance de paramètres de police statique. Il pourrait être consulté par [`DefaultInstance`](./defaultinstance) propriété.

La modification des paramètres de police est sécurisée à tout moment à partir de n'importe quel fil. Mais il est recommandé de ne pas modifier les paramètres de police lors du traitement de certains documents utilisant ces paramètres. Cela peut conduire au fait que la même police sera résolue différemment dans différentes parties du document.

### Exemples

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

// Il manque à la source de police par défaut deux des polices que nous utilisons dans notre document.
// Lorsque nous enregistrons ce document, Aspose.Words appliquera des polices de secours à tout le texte formaté avec des polices inaccessibles.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Crée une source de polices à partir d'un dossier contenant des polices.
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

// Restaure les sources de polices d'origine.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Montre comment définir un répertoire source de polices.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Nos sources de polices ne contiennent pas la police que nous avons utilisée pour le texte de ce document.
// Si nous utilisons ces paramètres de police lors du rendu de ce document,
// Aspose.Words appliquera une police de secours au texte qui a une police qu'Aspose.Words ne peut pas localiser.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Les sources de polices par défaut ne contiennent pas les deux polices que nous utilisons dans ce document.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Utilisez la méthode "SetFontsFolder" pour définir un répertoire qui agira comme une nouvelle source de police.
// Passez "false" comme argument "récursif" pour inclure les polices de tous les fichiers de polices qui se trouvent dans le répertoire
// que nous transmettons dans le premier argument, mais n'incluons aucune police dans aucun des sous-dossiers de ce répertoire.
// Passez "true" comme argument "récursif" pour inclure tous les fichiers de polices dans le répertoire que nous passons
// dans le premier argument, ainsi que toutes les polices dans ses sous-répertoires.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// La police "Amethysta" se trouve dans un sous-dossier du répertoire des polices.
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

// Restaure les sources de polices d'origine.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Montre comment définir plusieurs répertoires source de polices.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Nos sources de polices ne contiennent pas la police que nous avons utilisée pour le texte de ce document.
// Si nous utilisons ces paramètres de police lors du rendu de ce document,
// Aspose.Words appliquera une police de secours au texte qui a une police qu'Aspose.Words ne peut pas localiser.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Les sources de polices par défaut ne contiennent pas les deux polices que nous utilisons dans ce document.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Utilisez la méthode "SetFontsFolders" pour créer une source de polices à partir de chaque répertoire de polices que nous passons comme premier argument.
// Passez "false" comme argument "récursif" pour inclure les polices de tous les fichiers de polices qui se trouvent dans les répertoires
// que nous transmettons dans le premier argument, mais n'incluons aucune police d'aucun des sous-dossiers des répertoires.
// Passez "true" comme argument "récursif" pour inclure tous les fichiers de polices dans les répertoires que nous passons
// dans le premier argument, ainsi que toutes les polices dans leurs sous-répertoires.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Le dossier "Junction" lui-même ne contient pas de fichiers de polices, mais des sous-dossiers en contiennent.
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

// Restaure les sources de polices d'origine.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Voir également

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
