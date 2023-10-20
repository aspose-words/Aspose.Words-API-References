---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words per .NET
description: MarkdownSaveOptions ImagesFolderAlias proprietà. Specifica il nome della cartella utilizzata per costruire gli URI di immagine scritti in un documento. Il valore predefinito è una stringa vuota in C#.
type: docs
weight: 50
url: /it/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI di immagine scritti in un documento. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un file[`Document`](../../../aspose.words/document/) InMarkdown format, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [`ImagesFolder`](../imagesfolder/) ti permette di specificare dove verranno salvate le immagini e `ImagesFolderAlias` permette di specificare come verranno costruiti gli URI dell'immagine.

Se`ImagesFolderAlias` non è una stringa vuota, lo sarà l'URI dell'immagine scritto in MarkdownImagesFolderAlias + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias` è una stringa vuota, l'URI dell'immagine scritto in Markdown saràCartella Immagini + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias`è impostato per '.' (punto), il nome del file immagine verrà scritto in Markdown senza percorso indipendentemente dalle altre opzioni.

## Esempi

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
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
