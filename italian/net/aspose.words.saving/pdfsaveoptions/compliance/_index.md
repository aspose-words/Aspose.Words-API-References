---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words per .NET
description: Scopri la proprietà di conformità PdfSaveOptions per garantire che i tuoi documenti PDF soddisfino gli standard di settore in termini di qualità e compatibilità.
type: docs
weight: 50
url: /it/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Specifica il livello di conformità agli standard PDF per i documenti di output.

```csharp
public PdfCompliance Compliance { get; set; }
```

## Osservazioni

Il valore predefinito èPdf17.

## Esempi

Mostra come impostare il livello di conformità agli standard PDF dei documenti PDF salvati.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
// Nota che alcune PdfSaveOptions sono proibite quando si salva in uno degli standard e vengono corrette automaticamente.
// Utilizzare IWarningCallback per sapere quali opzioni vengono corrette automaticamente.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Impostare la proprietà "Compliance" su "PdfCompliance.PdfA1b" per conformarsi allo standard "PDF/A-1b",
// che mira a preservare l'aspetto visivo del documento mentre Aspose.Words lo converte in PDF.
// Impostare la proprietà "Compliance" su "PdfCompliance.Pdf17" per conformarsi allo standard "1.7".
// Impostare la proprietà "Compliance" su "PdfCompliance.PdfA1a" per conformarsi allo standard "PDF/A-1a",
// che è conforme allo standard "PDF/A-1b" e allo stesso tempo preserva la struttura del documento originale.
// Impostare la proprietà "Compliance" su "PdfCompliance.PdfUa1" per conformarsi allo standard "PDF/UA-1" (ISO 14289-1),
// che mira a definire la rappresentazione dei documenti elettronici in formato PDF che consentono l'accesso al file.
// Impostare la proprietà "Compliance" su "PdfCompliance.Pdf20" per conformarsi allo standard "PDF 2.0" (ISO 32000-2).
// Impostare la proprietà "Compliance" su "PdfCompliance.PdfA4" per conformarsi allo standard "PDF/A-4" (ISO 19004:2020),
// che preserva l'aspetto visivo statico del documento nel tempo.
// Impostare la proprietà "Compliance" su "PdfCompliance.PdfA4Ua2" per essere conforme a PDF/A-4 (ISO 19005-4:2020)
// e standard PDF/UA-2 (ISO 14289-2:2024).
// Impostare la proprietà "Compliance" su "PdfCompliance.PdfUa2" per conformarsi allo standard PDF/UA-2 (ISO 14289-2:2024).
// Ciò aiuta a rendere i documenti ricercabili, ma potrebbe aumentare significativamente le dimensioni di documenti già di grandi dimensioni.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Guarda anche

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
