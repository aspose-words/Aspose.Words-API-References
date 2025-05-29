---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words per .NET
description: Ottimizza le tue immagini PDF con la proprietà JpegQuality di PdfSaveOptions, che ti consente di controllare la qualità JPEG per ottenere documenti visivi straordinari.
type: docs
weight: 220
url: /it/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento PDF.

```csharp
public int JpegQuality { get; set; }
```

## Osservazioni

Il valore predefinito è 100.

Questa proprietà viene utilizzata insieme a[`ImageCompression`](../imagecompression/) opzione.

Ha effetto solo se un documento contiene immagini JPEG.

Utilizzare questa proprietà per ottenere o impostare la qualità delle immagini all'interno di un documento quando si salva in formato PDF. Il valore può variare da 0 a 100, dove 0 indica la qualità peggiore ma la massima compressione e 100 indica la qualità migliore ma la minima compressione. Se la qualità è 100 e l'immagine sorgente è JPEG, significa nessuna compressione: verranno salvati i byte originali.

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

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
