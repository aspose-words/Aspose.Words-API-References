---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ResourceFolder de HtmlSaveOptions pour une exportation optimale de vos documents. Gérez facilement les images, les polices et les feuilles de style CSS dans un dossier dédié.
type: docs
weight: 440
url: /fr/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Spécifie un dossier physique où sont enregistrées toutes les ressources (images, polices et CSS externes) lors de l'exportation d'un document au format HTML. La valeur par défaut est une chaîne vide.

```csharp
public string ResourceFolder { get; set; }
```

## Remarques

`ResourceFolder` est le moyen le plus simple de spécifier un dossier dans lequel toutes les ressources doivent être écrites. Une autre façon est d'utiliser des propriétés individuelles[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , et[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` a une priorité inférieure à celle des dossiers spécifiés via[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , et[`CssStyleSheetFileName`](../cssstylesheetfilename/) . Par exemple, si both `ResourceFolder` et[`FontsFolder`](../fontsfolder/)sont spécifiés, les polices seront enregistrées dans[`FontsFolder`](../fontsfolder/) , tandis que les images et le CSS seront enregistrés dans`ResourceFolder`.

Si le dossier spécifié par`ResourceFolder` n'existe pas, il sera créé automatiquement.

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
