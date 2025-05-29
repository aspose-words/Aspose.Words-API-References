---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ImagesFolder di MarkdownSaveOptions migliora le esportazioni dei tuoi documenti specificando la cartella ideale in cui salvare le immagini in formato Markdown.
type: docs
weight: 80
url: /it/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Specifica la cartella fisica in cui vengono salvate le immagini quando si esporta un documento in Markdown formato. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolder { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) InMarkdownformato, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. `ImagesFolder` consente di specificare dove verranno salvate le immagini.

Se si salva un documento in un file e si fornisce un nome file, Aspose.Words, per impostazione predefinita, salva le immagini in la stessa cartella in cui è salvato il file del documento. Utilizzare`ImagesFolder` per ignorare questo comportamento.

Se si salva un documento in un flusso, Aspose.Words non ha una cartella in cui salvare le immagini, ma deve comunque salvarle da qualche parte. In questo caso, è necessario specificare una cartella accessibile nel`ImagesFolder` proprietà.

Se la cartella specificata da`ImagesFolder` non esiste, verrà creato automaticamente.

## Esempi

Mostra come specificare il nome della cartella utilizzata per costruire gli URI delle immagini.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilizzare la proprietà "ImagesFolder" per assegnare una cartella nel file system locale in cui
// Aspose.Words salverà tutte le immagini collegate del documento.
saveOptions.ImagesFolder = imagesFolder;
// Utilizzare la proprietà "ImagesFolderAlias" per utilizzare questa cartella
// quando si costruiscono gli URI delle immagini invece del nome della cartella delle immagini.
saveOptions.ImagesFolderAlias = "http://esempio.com/immagini";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Guarda anche

* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
