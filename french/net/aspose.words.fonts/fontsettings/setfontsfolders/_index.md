---
title: FontSettings.SetFontsFolders
second_title: Référence de l'API Aspose.Words pour .NET
description: FontSettings méthode. Définit les dossiers dans lesquels Aspose.Words recherche les polices TrueType lors du rendu de documents ou de lintégration de polices.
type: docs
weight: 90
url: /fr/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Définit les dossiers dans lesquels Aspose.Words recherche les polices TrueType lors du rendu de documents ou de l'intégration de polices.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fontsFolders | String[] | Tableau de dossiers contenant des polices TrueType. |
| recursive | Boolean | True pour analyser les dossiers spécifiés à la recherche de polices de manière récursive. |

### Remarques

Par défaut, Aspose.Words recherche les polices installées sur le système.

La définition de cette propriété réinitialise le cache de toutes les polices précédemment chargées.

### Exemples

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

* class [FontSettings](../)
* espace de noms [Aspose.Words.Fonts](../../fontsettings/)
* Assemblée [Aspose.Words](../../../)


