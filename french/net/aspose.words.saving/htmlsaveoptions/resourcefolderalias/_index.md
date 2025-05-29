---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words pour .NET
description: Optimisez vos documents HTML avec la propriété ResourceFolderAlias de HtmlSaveOptions, définissant des noms de dossiers pour une construction URI efficace des ressources.
type: docs
weight: 450
url: /fr/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI de toutes les ressources écrites dans un document HTML. La valeur par défaut est une chaîne vide.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Remarques

`ResourceFolderAlias` Il s'agit du moyen le plus simple de spécifier la manière dont les URI de tous les fichiers de ressources doivent être construites. Les mêmes informations peuvent être spécifiées séparément pour les images et les polices via[`ImagesFolderAlias`](../imagesfolderalias/) et[`FontsFolderAlias`](../fontsfolderalias/) propriétés, respectivement. Cependant, il n'existe pas de propriété spécifique pour CSS.

`ResourceFolderAlias` a une priorité inférieure à[`FontsFolderAlias`](../fontsfolderalias/) et[`ImagesFolderAlias`](../imagesfolderalias/) . Par exemple, si les deux`ResourceFolderAlias` et[`FontsFolderAlias`](../fontsfolderalias/) sont spécifiés, les URI des polices seront construits en utilisant [`FontsFolderAlias`](../fontsfolderalias/) tandis que les URI des images et CSS seront construits en utilisant `ResourceFolderAlias`.

Si`ResourceFolderAlias` est vide, le[`ResourceFolder`](../resourcefolder/) la valeur de la propriété sera utilisée pour construire les URI de ressources.

Si`ResourceFolderAlias` est défini sur '.' (point), les URI de ressources contiendront uniquement les noms de fichiers, sans aucun chemin.

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
