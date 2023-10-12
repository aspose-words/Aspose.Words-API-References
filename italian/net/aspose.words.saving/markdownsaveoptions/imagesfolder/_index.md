---
title: MarkdownSaveOptions.ImagesFolder
second_title: Aspose.Words per .NET API Reference
description: MarkdownSaveOptions proprietà. Specifica la cartella fisica in cui vengono salvate le immagini quando si esporta un documento in Markdown formato. Limpostazione predefinita è una stringa vuota.
type: docs
weight: 40
url: /it/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Specifica la cartella fisica in cui vengono salvate le immagini quando si esporta un documento in Markdown formato. L'impostazione predefinita è una stringa vuota.

```csharp
public string ImagesFolder { get; set; }
```

### Osservazioni

Quando salvi un file[`Document`](../../../aspose.words/document/) InMarkdownformat, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. `ImagesFolder` ti permette di specificare dove verranno salvate le immagini.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini in la stessa cartella in cui è salvato il file del documento. Utilizzo`ImagesFolder` per ignorare questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non ha una cartella dove salvare le immagini, ma deve comunque salvare le immagini da qualche parte. In questo caso, devi specificare una cartella accessibile nel file`ImagesFolder` proprietà.

Se la cartella specificata da`ImagesFolder` non esiste, verrà creato automaticamente.

### Esempi

Mostra come specificare il nome della cartella utilizzata per costruire URI di immagine.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilizzare la proprietà "ImagesFolder" per assegnare una cartella nel file system locale in cui
// Aspose.Words salverà tutte le immagini collegate del documento.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Utilizzare la proprietà "ImagesFolderAlias" per utilizzare questa cartella
// quando si costruiscono URI di immagine invece del nome della cartella delle immagini.
saveOptions.ImagesFolderAlias = "http://esempio.com/immagini";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

Mostra come specificare il nome della cartella utilizzata per costruire URI di immagine (.NetStandard 2.0).

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilizzare la proprietà "ImagesFolder" per assegnare una cartella nel file system locale in cui
// Aspose.Words salverà tutte le immagini collegate del documento.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Utilizzare la proprietà "ImagesFolderAlias" per utilizzare questa cartella
// quando si costruiscono URI di immagine invece del nome della cartella delle immagini.
saveOptions.ImagesFolderAlias = "http://esempio.com/immagini";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Guarda anche

* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../markdownsaveoptions/)
* assemblea [Aspose.Words](../../../)


