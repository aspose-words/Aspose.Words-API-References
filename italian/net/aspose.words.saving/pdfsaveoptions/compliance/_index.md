---
title: PdfSaveOptions.Compliance
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Specifica il livello di conformità agli standard PDF per i documenti di output.
type: docs
weight: 40
url: /it/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Specifica il livello di conformità agli standard PDF per i documenti di output.

```csharp
public PdfCompliance Compliance { get; set; }
```

### Osservazioni

L'impostazione predefinita èPdf17.

### Esempi

Mostra come impostare il livello di conformità agli standard PDF dei documenti PDF salvati.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
// Tieni presente che alcune PdfSaveOptions sono vietate durante il salvataggio in uno degli standard e vengono riparate automaticamente.
// Utilizza IWarningCallback per sapere quali opzioni vengono corrette automaticamente.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Imposta la proprietà "Compliance" su "PdfCompliance.PdfA1b" per conformarsi allo standard "PDF/A-1b",
// che mira a preservare l'aspetto visivo del documento mentre Aspose.Words lo converte in PDF.
// Imposta la proprietà "Compliance" su "PdfCompliance.Pdf17" per conformarsi allo standard "1.7".
// Imposta la proprietà "Conformità" su "PdfCompliance.PdfA1a" per conformarsi allo standard "PDF/A-1a",
// che è conforme a "PDF/A-1b" e preserva la struttura del documento originale.
// Imposta la proprietà "Compliance" su "PdfCompliance.PdfUa1" per conformarsi allo standard "PDF/UA-1" (ISO 14289-1),
// che mira a definire i documenti elettronici in PDF che consentono l'accesso al file.
// Imposta la proprietà "Conformità" su "PdfCompliance.Pdf20" per conformarsi allo standard "PDF 2.0" (ISO 32000-2).
// Imposta la proprietà "Conformità" su "PdfCompliance.PdfA4" per conformarsi allo standard "PDF/A-4" (ISO 19004:2020),
// che preservano l'aspetto visivo statico del documento nel tempo.
// Ciò aiuta a rendere i documenti ricercabili ma può aumentare significativamente la dimensione di documenti già di grandi dimensioni.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Guarda anche

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


