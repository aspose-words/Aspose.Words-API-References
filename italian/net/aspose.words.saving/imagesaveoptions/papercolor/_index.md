---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: Aspose.Words per .NET
description: ImageSaveOptions PaperColor proprietà. Ottiene o imposta il colore di sfondo carta per le immagini generate in C#.
type: docs
weight: 110
url: /it/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Ottiene o imposta il colore di sfondo (carta) per le immagini generate.

Il valore predefinito èWhite.

```csharp
public Color PaperColor { get; set; }
```

## Osservazioni

Quando si esegue il rendering delle pagine di un documento che specifica il proprio colore di sfondo, il colore di sfondo del documento sovrascriverà il colore specificato da questa proprietà.

## Esempi

Trasforma una pagina di un documento Word in un'immagine con sfondo trasparente o colorato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo trasforma il documento in un'immagine.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Imposta la proprietà "PaperColor" su un colore trasparente per applicare un colore trasparente
// sfondo del documento durante il rendering in un'immagine.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Imposta la proprietà "PaperColor" su un colore opaco per applicare quel colore
// come sfondo del documento mentre lo trasformiamo in un'immagine.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
