---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la méthode SetFontsFolder pour spécifier un répertoire de polices TrueType dans Aspose.Words, améliorant ainsi le rendu du document et l'incorporation des polices.
type: docs
weight: 80
url: /fr/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Définit le dossier dans lequel Aspose.Words recherche les polices TrueType lors du rendu de documents ou de l'incorporation de polices. Il s'agit d'un raccourci vers[`SetFontsFolders`](../setfontsfolders/) pour définir un seul répertoire de polices.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fontFolder | String | Le dossier qui contient les polices TrueType. |
| recursive | Boolean | Vrai pour analyser les dossiers spécifiés pour les polices de manière récursive. |

## Exemples

Montre comment définir un répertoire source de police.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Nos sources de polices ne contiennent pas la police que nous avons utilisée pour le texte de ce document.
// Si nous utilisons ces paramètres de police lors du rendu de ce document,
// Aspose.Words appliquera une police de secours au texte dont la police est introuvable dans Aspose.Words.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Les sources de polices par défaut ne contiennent pas les deux polices que nous utilisons dans ce document.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Utilisez la méthode « SetFontsFolder » pour définir un répertoire qui agira comme une nouvelle source de police.
// Passez « false » comme argument « recursive » pour inclure les polices de tous les fichiers de polices qui se trouvent dans le répertoire
// que nous transmettons dans le premier argument, mais n'incluons aucune police dans aucun des sous-dossiers de ce répertoire.
// Passez « true » comme argument « recursive » pour inclure tous les fichiers de polices dans le répertoire que nous transmettons
// dans le premier argument, ainsi que toutes les polices dans ses sous-répertoires.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// La police « Amethysta » se trouve dans un sous-dossier du répertoire des polices.
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

// Restaurer les sources de polices d'origine.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Voir également

* class [FontSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
