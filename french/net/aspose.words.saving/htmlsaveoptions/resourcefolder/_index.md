---
title: HtmlSaveOptions.ResourceFolder
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Spécifie un dossier physique dans lequel toutes les ressources telles que les images les polices et les CSS externes sont enregistrées lorsquun document est exporté au format HTML. La valeur par défaut est une chaîne vide.
type: docs
weight: 420
url: /fr/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Spécifie un dossier physique dans lequel toutes les ressources telles que les images, les polices et les CSS externes sont enregistrées lorsqu'un document est exporté au format HTML. La valeur par défaut est une chaîne vide.

```csharp
public string ResourceFolder { get; set; }
```

### Remarques

`ResourceFolder` est le moyen le plus simple de spécifier un dossier dans lequel toutes les ressources doivent être écrites. Une autre façon consiste à utiliser des propriétés individuelles[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , et[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` a une priorité inférieure aux dossiers spécifiés via[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , et[`CssStyleSheetFileName`](../cssstylesheetfilename/) . Par exemple, si Both `ResourceFolder` et[`FontsFolder`](../fontsfolder/)sont spécifiés, les polices seront enregistrées dans[`FontsFolder`](../fontsfolder/) , tandis que les images et CSS seront enregistrés dans`ResourceFolder`.

Si le dossier spécifié par`ResourceFolder` n'existe pas, il sera créé automatiquement.

### Exemples

Montre comment définir des dossiers et des alias de dossier pour les ressources enregistrées en externe qu'Aspose.Words créera lors de l'enregistrement d'un document au format HTML.

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
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


