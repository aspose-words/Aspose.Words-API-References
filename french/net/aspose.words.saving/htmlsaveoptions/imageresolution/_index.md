---
title: HtmlSaveOptions.ImageResolution
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Spécifie la résolution de sortie des images lors de lexportation au format HTML MHTML ou EPUB. La valeur par défaut est96 ppp .
type: docs
weight: 340
url: /fr/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Spécifie la résolution de sortie des images lors de l'exportation au format HTML, MHTML ou EPUB. La valeur par défaut est`96 ppp` .

```csharp
public int ImageResolution { get; set; }
```

### Remarques

Cette propriété affecte les images raster lorsque[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) est`vrai` et métafichiers d'effets exportés sous forme d'images raster. Certaines propriétés d'image telles que cropping ou rotation nécessitent l'enregistrement des images transformées et dans ce cas, les images transformées sont créées dans la résolution donnée .

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

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


