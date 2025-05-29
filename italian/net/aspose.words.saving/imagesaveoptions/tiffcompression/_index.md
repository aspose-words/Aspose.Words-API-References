---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words per .NET
description: Ottimizza le tue immagini TIFF con la proprietà TiffCompression di ImageSaveOptions, che ti consente di scegliere il metodo di compressione migliore per risultati di qualità.
type: docs
weight: 180
url: /it/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Ottiene o imposta il tipo di compressione da applicare durante il salvataggio delle immagini generate nel formato TIFF.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Osservazioni

Ha effetto solo se si salva in formato TIFF.

Il valore predefinito èLzw.

## Esempi

Mostra come selezionare lo schema di compressione da applicare a un documento che convertiamo in un'immagine TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// Creiamo un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo trasforma il documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// Imposta la proprietà "TiffCompression" su "TiffCompression.None" per non applicare alcuna compressione durante il salvataggio,
// che potrebbe generare un file di output molto grande.
// Imposta la proprietà "TiffCompression" su "TiffCompression.Rle" per applicare la compressione RLE
// Impostare la proprietà "TiffCompression" su "TiffCompression.Lzw" per applicare la compressione LZW.
// Impostare la proprietà "TiffCompression" su "TiffCompression.Ccitt3" per applicare la compressione CCITT3.
// Impostare la proprietà "TiffCompression" su "TiffCompression.Ccitt4" per applicare la compressione CCITT4.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### Guarda anche

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
