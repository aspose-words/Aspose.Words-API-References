---
title: PdfSaveOptions.JpegQuality
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Ottiene o imposta un valore che determina la qualità delle immagini JPEG allinterno del documento PDF.
type: docs
weight: 190
url: /it/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento PDF.

```csharp
public int JpegQuality { get; set; }
```

### Osservazioni

Il valore predefinito è 100.

Questa proprietà è utilizzata in combinazione con il[`ImageCompression`](../imagecompression/) opzione.

Ha effetto solo quando un documento contiene immagini JPEG.

Utilizzare questa proprietà per ottenere o impostare la qualità delle immagini all'interno di un documento durante il salvataggio in formato PDF. Il valore può variare da 0 a 100 dove 0 significa qualità peggiore ma compressione massima e 100 significa qualità migliore ma compressione minima. Se qualità è 100 e l'immagine di origine è JPEG, significa che non c'è compressione: i byte originali verranno salvati.

### Esempi

Mostra come specificare un tipo di compressione per tutte le immagini in un documento che stiamo convertendo in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Imposta la proprietà "ImageCompression" su "PdfImageCompression.Auto" per utilizzare il file
// Proprietà "ImageCompression" per controllare la qualità delle immagini Jpeg che finiscono nel PDF di output.
// Imposta la proprietà "ImageCompression" su "PdfImageCompression.Jpeg" per usare il file
// Proprietà "ImageCompression" per controllare la qualità di tutte le immagini che finiscono nel PDF di output.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Imposta la proprietà "JpegQuality" su "10" per rafforzare la compressione a scapito della qualità dell'immagine.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


