---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words per .NET
description: Scopri la proprietà ResourceFolder di HtmlSaveOptions per un'esportazione ottimale dei documenti. Gestisci facilmente immagini, font e CSS in una cartella dedicata.
type: docs
weight: 440
url: /it/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Specifica una cartella fisica in cui vengono salvate tutte le risorse come immagini, font e CSS esterni quando un documento viene esportato in HTML. Il valore predefinito è una stringa vuota.

```csharp
public string ResourceFolder { get; set; }
```

## Osservazioni

`ResourceFolder` è il modo più semplice per specificare una cartella in cui tutte le risorse devono essere scritte. Un altro modo è utilizzare le singole proprietà[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , e[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` ha una priorità inferiore rispetto alle cartelle specificate tramite[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , E[`CssStyleSheetFileName`](../cssstylesheetfilename/) Ad esempio, se both `ResourceFolder` E[`FontsFolder`](../fontsfolder/)sono specificati, i font verranno salvati in[`FontsFolder`](../fontsfolder/) , mentre le immagini e i CSS verranno salvati in`ResourceFolder`.

Se la cartella specificata da`ResourceFolder` non esiste, verrà creato automaticamente.

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
