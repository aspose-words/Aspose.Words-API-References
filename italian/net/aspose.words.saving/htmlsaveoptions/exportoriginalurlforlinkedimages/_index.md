---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words per .NET
description: Scopri la funzione ExportOriginalUrlForLinkedImages di HtmlSaveOptions, che ti consente di utilizzare gli URL originali per le immagini collegate. Migliora l'integrità del tuo documento!
type: docs
weight: 200
url: /it/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Specifica se l'URL originale deve essere utilizzato come URL delle immagini collegate. Il valore predefinito è`falso` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Osservazioni

Se il valore è impostato su`VERO`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) il valore è usato come URL delle immagini collegate e le immagini collegate non vengono caricate nella cartella del documento o[`ImagesFolder`](../imagesfolder/).

Se il valore è impostato su`falso`le immagini collegate vengono caricate nella cartella del documento o[`ImagesFolder`](../imagesfolder/) e l'URL di ogni immagine collegata viene costruito in base alla cartella del documento,[`ImagesFolder`](../imagesfolder/) e[`ImagesFolderAlias`](../imagesfolderalias/) proprietà.

## Esempi

Mostra come impostare cartelle e alias di cartelle per le risorse salvate esternamente che Aspose.Words creerà quando si salva un documento in HTML.

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
    FontsFolderAlias = "http://esempio.com/font",
    ImagesFolderAlias = "http://esempio.com/immagini",
    ResourceFolderAlias = "http://esempio.com/risorse",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
