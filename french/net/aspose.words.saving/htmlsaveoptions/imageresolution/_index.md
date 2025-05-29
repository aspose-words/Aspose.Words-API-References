---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words pour .NET
description: Ajustez facilement la résolution de vos images grâce à HtmlSaveOptions. Optimisez vos exportations HTML, MHTML ou EPUB grâce à des paramètres personnalisables pour des visuels époustouflants.
type: docs
weight: 340
url: /fr/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Spécifie la résolution de sortie des images lors de l'exportation au format HTML, MHTML ou EPUB. La valeur par défaut est`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Remarques

Cette propriété affecte les images raster lorsque[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) est`vrai` et les métafichiers d'effets exportés sous forme d'images raster. Certaines propriétés d'image, telles que le recadrage (x000d_) ou la rotation, nécessitent l'enregistrement des images transformées ; dans ce cas, les images transformées sont créées avec la résolution (x000d_).

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

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
