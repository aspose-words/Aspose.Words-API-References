---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HtmlSaveOptions ImagesFolderAlias pour gérer facilement les URI des images dans vos documents HTML. Simplifiez votre flux de travail grâce à cette fonctionnalité essentielle !
type: docs
weight: 370
url: /fr/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document HTML. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format HTML, Aspose.Words doit enregistrer toutes les images intégrées dans le document sous forme de fichiers autonomes.[`ImagesFolder`](../imagesfolder/) vous permet de spécifier où les images seront enregistrées et`ImagesFolderAlias` permet de spécifier comment les URI des images seront construits.

Si`ImagesFolderAlias` n'est pas une chaîne vide, alors l'URI de l'image written en HTML seraImagesFolderAlias + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias`est une chaîne vide, alors l'URI de l'image écrite en HTML seraImagesFolder + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias` est défini sur '.' (point), alors le nom du fichier image sera écrit en HTML sans chemin, quelles que soient les autres options.

Une autre façon de spécifier le nom du dossier pour construire les URI d'image est d'utiliser[`ResourceFolderAlias`](../resourcefolderalias/).

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
