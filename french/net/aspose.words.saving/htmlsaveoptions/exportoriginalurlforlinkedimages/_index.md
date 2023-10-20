---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ExportOriginalUrlForLinkedImages propriété. Spécifie si lURL dorigine doit être utilisée comme URL des images liées. La valeur par défaut estFAUX  en C#.
type: docs
weight: 200
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Spécifie si l'URL d'origine doit être utilisée comme URL des images liées. La valeur par défaut est`FAUX` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Remarques

Si la valeur est définie sur`vrai`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) la valeur est utilisée car l'URL des images liées et les images liées ne sont pas chargées dans le dossier du document ou[`ImagesFolder`](../imagesfolder/).

Si la valeur est définie sur`FAUX`les images liées sont chargées dans le dossier du document ou[`ImagesFolder`](../imagesfolder/) et l'URL de chaque image liée est construite en fonction du dossier du document,[`ImagesFolder`](../imagesfolder/) et[`ImagesFolderAlias`](../imagesfolderalias/) propriétés.

## Exemples

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
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
