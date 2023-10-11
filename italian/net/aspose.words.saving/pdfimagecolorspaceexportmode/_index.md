---
title: Enum PdfImageColorSpaceExportMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.PdfImageColorSpaceExportMode enum. Specifica come verrà selezionato lo spazio colore per le immagini nel documento PDF.
type: docs
weight: 5480
url: /it/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

Specifica come verrà selezionato lo spazio colore per le immagini nel documento PDF.

```csharp
public enum PdfImageColorSpaceExportMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `0` | Aspose.Words seleziona automaticamente lo spazio colore più appropriato per ciascuna immagine. |
| SimpleCmyk | `1` | Aspose.Words converte le immagini RGB nello spazio colore CMYK utilizzando una formula semplice. |

### Esempi

Mostra come impostare uno spazio colore diverso per le immagini in un documento mentre lo esportiamo in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Imposta la proprietà "ImageColorSpaceExportMode" su "PdfImageColorSpaceExportMode.Auto" per ottenere Aspose.Words su
// seleziona automaticamente lo spazio colore per le immagini nel documento che converte in PDF.
// Nella maggior parte dei casi, lo spazio colore sarà RGB.
// Imposta la proprietà "ImageColorSpaceExportMode" su "PdfImageColorSpaceExportMode.SimpleCmyk"
// per utilizzare lo spazio colore CMYK per tutte le immagini nel PDF salvato.
// Aspose.Words applicherà anche la compressione Flate a tutte le immagini e ignorerà il valore della proprietà "ImageCompression".
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


