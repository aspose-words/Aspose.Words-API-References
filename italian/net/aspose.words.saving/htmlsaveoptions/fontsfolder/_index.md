---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words per .NET
description: HtmlSaveOptions FontsFolder proprietà. Specifica la cartella fisica in cui vengono salvati i caratteri durante lesportazione di un documento in HTML. Limpostazione predefinita è una stringa vuota in C#.
type: docs
weight: 310
url: /it/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Specifica la cartella fisica in cui vengono salvati i caratteri durante l'esportazione di un documento in HTML. L'impostazione predefinita è una stringa vuota.

```csharp
public string FontsFolder { get; set; }
```

## Osservazioni

Quando salvi un file[`Document`](../../../aspose.words/document/) in formato HTML e[`ExportFontResources`](../exportfontresources/) è impostato su`VERO` , Aspose.Words deve salvare i caratteri utilizzati nel documento come file autonomi. `FontsFolder` ti permette di specificare dove verranno salvati i caratteri e [`FontsFolderAlias`](../fontsfolderalias/) permette di specificare come verranno costruiti gli URI dei caratteri.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva i caratteri nella stessa cartella in cui è salvato il file del documento. Utilizzo`FontsFolder` per sovrascrivere questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non ha una cartella in cui salvare i caratteri, ma deve comunque salvare i caratteri da qualche parte. In questo caso, devi specificare una cartella accessibile nel file`FontsFolder` proprietà o fornire flussi personalizzati tramite the[`FontSavingCallback`](../fontsavingcallback/) gestore di eventi.

Se la cartella specificata da`FontsFolder` non esiste, verrà creato automaticamente.

[`ResourceFolder`](../resourcefolder/) è un altro modo per specificare una cartella in cui salvare i caratteri.

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

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
