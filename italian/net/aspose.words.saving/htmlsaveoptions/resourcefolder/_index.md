---
title: HtmlSaveOptions.ResourceFolder
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica una cartella fisica in cui vengono salvate tutte le risorse come immagini caratteri e CSS esterni quando un documento viene esportato in HTML. Limpostazione predefinita è una stringa vuota.
type: docs
weight: 420
url: /it/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Specifica una cartella fisica in cui vengono salvate tutte le risorse come immagini, caratteri e CSS esterni quando un documento viene esportato in HTML. L'impostazione predefinita è una stringa vuota.

```csharp
public string ResourceFolder { get; set; }
```

### Osservazioni

`ResourceFolder` è il modo più semplice per specificare una cartella in cui scrivere tutte le risorse. Un altro modo è utilizzare le singole proprietà[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , e[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` ha una priorità inferiore rispetto alle cartelle specificate tramite[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , E[`CssStyleSheetFileName`](../cssstylesheetfilename/) . Ad esempio, se entrambi `ResourceFolder` E[`FontsFolder`](../fontsfolder/)sono specificati, i caratteri verranno salvati in[`FontsFolder`](../fontsfolder/) , mentre le immagini e i CSS verranno salvati in`ResourceFolder`.

Se la cartella specificata da`ResourceFolder` non esiste, verrà creato automaticamente.

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
    FontsFolderAlias = "http://esempio.com/fonts",
    ImagesFolderAlias = "http://esempio.com/immagini",
    ResourceFolderAlias = "http://esempio.com/risorse",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


