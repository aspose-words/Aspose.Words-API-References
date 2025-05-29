---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words per .NET
description: Regola la risoluzione delle immagini senza sforzo con HtmlSaveOptions. Ottimizza le tue esportazioni HTML, MHTML o EPUB con impostazioni personalizzabili per immagini straordinarie.
type: docs
weight: 340
url: /it/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Specifica la risoluzione di output per le immagini durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Osservazioni

Questa proprietà influisce sulle immagini raster quando[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) è`VERO` e metafile di effetti esportati come immagini raster. Alcune proprietà delle immagini, come il ritaglio o la rotazione, richiedono il salvataggio delle immagini trasformate e, in questo caso, le immagini trasformate vengono create nella risoluzione specificata.

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

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
