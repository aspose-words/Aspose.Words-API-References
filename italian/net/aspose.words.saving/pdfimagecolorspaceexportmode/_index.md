---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words PdfImageColorSpaceExportMode per ottimizzare la selezione dei colori delle immagini nei tuoi documenti PDF, ottenendo risultati visivi straordinari.
type: docs
weight: 6270
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
| Auto | `0` | Aspose.Words seleziona automaticamente lo spazio colore più appropriato per ogni immagine. |
| SimpleCmyk | `1` | Aspose.Words converte le immagini RGB nello spazio colore CMYK utilizzando una semplice formula. |

## Esempi

Mostra come impostare uno spazio colore diverso per le immagini in un documento quando lo esportiamo in PDF.

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
