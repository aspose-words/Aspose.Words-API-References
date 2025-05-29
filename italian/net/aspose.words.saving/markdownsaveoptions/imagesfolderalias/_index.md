---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImagesFolderAlias di MarkdownSaveOptions per gestire facilmente gli URI delle immagini nei tuoi documenti. Semplifica il tuo flusso di lavoro con questa funzionalità essenziale!
type: docs
weight: 90
url: /it/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI delle immagini scritti in un documento. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) InMarkdown formato, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [`ImagesFolder`](../imagesfolder/) consente di specificare dove verranno salvate le immagini e `ImagesFolderAlias` consente di specificare come verranno costruiti gli URI delle immagini.

Se`ImagesFolderAlias` non è una stringa vuota, allora l'URI dell'immagine scritto in Markdown saràImagesFolderAlias + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias` è una stringa vuota, quindi l'URI dell'immagine scritto in Markdown saràImagesFolder + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias` è impostato su '.' (punto), il file immagine name verrà scritto in Markdown senza percorso, indipendentemente dalle altre opzioni.

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
