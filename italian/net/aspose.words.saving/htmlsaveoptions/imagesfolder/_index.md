---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImagesFolder di HtmlSaveOptions. Imposta facilmente la cartella in cui salvare le immagini durante l'esportazione di documenti in HTML. Semplifica il tuo flusso di lavoro oggi stesso!
type: docs
weight: 360
url: /it/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Specifica la cartella fisica in cui vengono salvate le immagini durante l'esportazione di un documento in formato HTML. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolder { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) in formato HTML, Aspose.Words deve salvare tutte le immagini x000d incorporate nel documento come file autonomi.`ImagesFolder` consente di specificare dove verranno salvate le immagini e[`ImagesFolderAlias`](../imagesfolderalias/) consente di specificare come verranno costruiti gli URI delle immagini.

Se si salva un documento in un file e si fornisce un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Utilizzare`ImagesFolder` per ignorare questo comportamento.

Se si salva un documento in un flusso, Aspose.Words non ha una cartella in cui salvare le immagini, , ma deve comunque salvarle da qualche parte. In questo caso, è necessario specificare una cartella accessibile nel`ImagesFolder` proprietà o fornire flussi personalizzati tramite [`ImageSavingCallback`](../imagesavingcallback/) gestore degli eventi.

Se la cartella specificata da`ImagesFolder` non esiste, verrà creato automaticamente.

[`ResourceFolder`](../resourcefolder/) è un altro modo per specificare una cartella in cui salvare le immagini.

## Esempi

Mostra come specificare la cartella in cui archiviare le immagini collegate dopo averle salvate in formato .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Imposta un'opzione per esportare i campi del modulo come testo normale anziché come elementi di input HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
