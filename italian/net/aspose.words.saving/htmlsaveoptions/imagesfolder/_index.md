---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ImagesFolder proprietà. Specifica la cartella fisica in cui vengono salvate le immagini durante lesportazione di un documento in formato HTML. Il valore predefinito è una stringa vuota in C#.
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

Quando salvi un file[`Document`](../../../aspose.words/document/) in formato HTML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi.`ImagesFolder` ti consente di specificare dove verranno salvate le immagini e[`ImagesFolderAlias`](../imagesfolderalias/) consente di specificare come verranno costruiti gli URI dell'immagine.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Utilizzo`ImagesFolder` per sovrascrivere questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non ha una cartella in cui salvare le immagini, ma deve comunque salvare le immagini da qualche parte. In questo caso, devi specificare una cartella accessibile nel file`ImagesFolder` proprietà o fornire flussi personalizzati tramite the[`ImageSavingCallback`](../imagesavingcallback/) gestore di eventi.

Se la cartella specificata da`ImagesFolder` non esiste, verrà creato automaticamente.

[`ResourceFolder`](../resourcefolder/) è un altro modo per specificare una cartella in cui salvare le immagini.

## Esempi

Mostra come specificare la cartella per la memorizzazione delle immagini collegate dopo il salvataggio in .html.

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
