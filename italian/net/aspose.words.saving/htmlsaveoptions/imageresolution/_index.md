---
title: ImageResolution
second_title: Aspose.Words per .NET API Reference
description: Specifica la risoluzione di output per le immagini durante lesportazione in HTML MHTML o EPUB. Limpostazione predefinita è96 dpi .
type: docs
weight: 350
url: /it/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Specifica la risoluzione di output per le immagini durante l'esportazione in HTML, MHTML o EPUB. L'impostazione predefinita è`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

### Osservazioni

Questa proprietà ha effetto sulle immagini raster quando[`ScaleImageToShapeSize`](../scaleimagetoshapesize) è`VERO` ed effetti metafile esportati come immagini raster. Alcune proprietà dell'immagine come il ritaglio o la rotazione richiedono il salvataggio delle immagini trasformate e in questo caso le immagini trasformate vengono create con la risoluzione data .

### Esempi

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
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://esempio.com/risorse",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Guarda anche

* property [ScaleImageToShapeSize](../scaleimagetoshapesize)
* class [HtmlSaveOptions](../../htmlsaveoptions)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
