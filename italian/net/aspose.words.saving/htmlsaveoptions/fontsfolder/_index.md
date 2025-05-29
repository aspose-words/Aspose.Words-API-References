---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontsFolder di HtmlSaveOptions per gestire facilmente l'archiviazione dei font per le esportazioni HTML, migliorando la presentazione e l'accessibilità dei documenti.
type: docs
weight: 310
url: /it/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Specifica la cartella fisica in cui vengono salvati i font quando si esporta un documento in HTML. Il valore predefinito è una stringa vuota.

```csharp
public string FontsFolder { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) in formato HTML e[`ExportFontResources`](../exportfontresources/) è impostato su`VERO` , Aspose.Words deve salvare i font utilizzati nel documento come file autonomi. `FontsFolder` consente di specificare dove verranno salvati i font e [`FontsFolderAlias`](../fontsfolderalias/) consente di specificare come verranno costruiti gli URI dei font.

Se si salva un documento in un file e si specifica un nome file, Aspose.Words, per impostazione predefinita, salva i font nella stessa cartella in cui è salvato il file del documento. Utilizzare`FontsFolder` per ignorare questo comportamento.

Se si salva un documento in un flusso, Aspose.Words non ha una cartella in cui salvare i font, , ma deve comunque salvarli da qualche parte. In questo caso, è necessario specificare una cartella accessibile nel`FontsFolder` proprietà o fornire flussi personalizzati tramite [`FontSavingCallback`](../fontsavingcallback/) gestore degli eventi.

Se la cartella specificata da`FontsFolder` non esiste, verrà creato automaticamente.

[`ResourceFolder`](../resourcefolder/) è un altro modo per specificare una cartella in cui salvare i font.

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
