---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ImageResolution proprietà. Specifica la risoluzione di output per le immagini durante lesportazione in HTML MHTML o EPUB. Limpostazione predefinita è96 dpi  in C#.
type: docs
weight: 340
url: /it/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Specifica la risoluzione di output per le immagini durante l'esportazione in HTML, MHTML o EPUB. L'impostazione predefinita è`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Osservazioni

Questa proprietà influisce sulle immagini raster quando[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) è`VERO` e metafile degli effetti esportati come immagini raster. Alcune proprietà dell'immagine come ritaglio o rotazione richiedono il salvataggio delle immagini trasformate e in questo caso le immagini trasformate vengono create nella risoluzione specificata.

## Esempi

Mostra come impostare cartelle e alias di cartelle per le risorse salvate esternamente che Aspose.Words creerà durante il salvataggio di un documento in HTML.

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
    FontsFolderAlias = "http://esempio.com/fonts",
    ImagesFolderAlias = "http://esempio.com/immagini",
    ResourceFolderAlias = "http://esempio.com/risorse",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Guarda anche

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
