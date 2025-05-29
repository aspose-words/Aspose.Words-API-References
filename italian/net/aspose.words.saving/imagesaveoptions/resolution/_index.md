---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words per .NET
description: Ottimizza le tue immagini con ImageSaveOptions! Controlla la risoluzione orizzontale e verticale in DPI per una qualità e una nitidezza straordinarie. Migliora le tue immagini oggi stesso!
type: docs
weight: 130
url: /it/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Imposta la risoluzione orizzontale e verticale per le immagini generate, in punti per pollice.

```csharp
public float Resolution { set; }
```

## Osservazioni

Questa proprietà ha effetto solo quando si salva in formati di immagini raster.

## Esempi

Mostra come specificare una risoluzione durante il rendering di un documento in formato PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Creiamo un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo trasforma il documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Impostare la proprietà "Risoluzione" su "72" per visualizzare il documento a 72 dpi.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Impostare la proprietà "Risoluzione" su "300" per visualizzare il documento a 300 dpi.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
