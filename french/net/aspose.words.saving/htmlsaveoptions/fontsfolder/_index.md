---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HtmlSaveOptions FontsFolder pour gérer facilement le stockage des polices pour les exportations HTML, améliorant ainsi la présentation et l'accessibilité des documents.
type: docs
weight: 310
url: /fr/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Spécifie le dossier physique dans lequel les polices sont enregistrées lors de l'exportation d'un document au format HTML. La valeur par défaut est une chaîne vide.

```csharp
public string FontsFolder { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format HTML et[`ExportFontResources`](../exportfontresources/) est défini sur`vrai` Aspose.Words doit enregistrer les polices utilisées dans le document sous forme de fichiers autonomes. `FontsFolder` vous permet de spécifier où les polices seront enregistrées et [`FontsFolderAlias`](../fontsfolderalias/) permet de spécifier comment les URI des polices seront construites.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les polices dans le même dossier où le fichier du document est enregistré.`FontsFolder` pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words ne dispose pas de dossier pour enregistrer les polices, mais doit tout de même les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible, dans le fichier`FontsFolder` propriété ou fournir des flux personnalisés via le[`FontSavingCallback`](../fontsavingcallback/) gestionnaire d'événements.

Si le dossier spécifié par`FontsFolder` n'existe pas, il sera créé automatiquement.

[`ResourceFolder`](../resourcefolder/) est une autre façon de spécifier un dossier dans lequel les polices doivent être enregistrées.

## Exemples

Montre comment définir des dossiers et des alias de dossiers pour les ressources enregistrées en externe qu'Aspose.Words créera lors de l'enregistrement d'un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://exemple.com/fonts",
    ImagesFolderAlias = "http://exemple.com/images",
    ResourceFolderAlias = "http://exemple.com/ressources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
