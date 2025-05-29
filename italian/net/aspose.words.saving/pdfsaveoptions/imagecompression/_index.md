---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words per .NET
description: Ottimizza il tuo PDF con la proprietà ImageCompression di PdfSaveOptions, che ti consente di scegliere il tipo di compressione migliore per immagini vivide e di alta qualità.
type: docs
weight: 200
url: /it/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Specifica il tipo di compressione da utilizzare per tutte le immagini nel documento.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## Osservazioni

Il valore predefinito èAuto.

UtilizzoJpeg consente di controllare la qualità delle immagini nel documento di output tramite[`JpegQuality`](../jpegquality/) proprietà.

UtilizzoJpeg fornisce la velocità di conversione più rapida se confrontata con le prestazioni di altri tipi di compressione, ma in questo caso si tratta di una compressione JPEG con perdita di dati.

UtilizzoAuto consente di controllare la qualità del Jpeg nel documento di output tramite[`JpegQuality`](../jpegquality/)proprietà, ma per altri formati, i dati pixel grezzi vengono estratti e salvati con la compressione Flate. Questo caso è più lento della conversione Jpeg ma senza perdite.

## Esempi

Mostra come specificare un tipo di compressione per tutte le immagini in un documento che stiamo convertendo in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
// Impostare la proprietà "ImageCompression" su "PdfImageCompression.Auto" per utilizzare
// Proprietà "ImageCompression" per controllare la qualità delle immagini Jpeg che finiscono nel PDF di output.
// Imposta la proprietà "ImageCompression" su "PdfImageCompression.Jpeg" per utilizzare
// Proprietà "ImageCompression" per controllare la qualità di tutte le immagini che finiscono nel PDF di output.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// Impostare la proprietà "JpegQuality" su "10" per rafforzare la compressione a scapito della qualità dell'immagine.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Guarda anche

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
