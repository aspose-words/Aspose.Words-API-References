---
title: HtmlSaveOptions.FontsFolder
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica la cartella fisica in cui vengono salvati i caratteri durante lesportazione di un documento in HTML. Limpostazione predefinita è una stringa vuota.
type: docs
weight: 320
url: /it/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Specifica la cartella fisica in cui vengono salvati i caratteri durante l'esportazione di un documento in HTML. L'impostazione predefinita è una stringa vuota.

```csharp
public string FontsFolder { get; set; }
```

### Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) in formato HTML e[`ExportFontResources`](../exportfontresources/) è impostato su`VERO` , Aspose.Words deve salvare i caratteri utilizzati nel documento come file autonomi. `FontsFolder` consente di specificare dove verranno salvati i caratteri e [`FontsFolderAlias`](../fontsfolderalias/) consente di specificare come verranno costruiti gli URI dei font.

Se si salva un documento in un file e si fornisce un nome file, Aspose.Words, per impostazione predefinita, salva i caratteri nella stessa cartella in cui è stato salvato il file del documento. Uso`FontsFolder` per ignorare questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non ha una cartella in cui salvare i caratteri, , ma deve comunque salvare i caratteri da qualche parte. In questo caso, è necessario specificare una cartella accessibile nel file`FontsFolder` proprietà o fornire flussi personalizzati tramite the[`FontSavingCallback`](../fontsavingcallback/) gestore di eventi.

Se la cartella specificata da`FontsFolder` non esiste, verrà creato automaticamente.

[`ResourceFolder`](../resourcefolder/) è un altro modo per specificare una cartella in cui salvare i caratteri.

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

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


