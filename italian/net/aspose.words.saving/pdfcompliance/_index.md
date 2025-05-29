---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.PdfCompliance per migliorare la conformità agli standard PDF. Migliora la qualità dei tuoi documenti con opzioni personalizzate per ogni esigenza!
type: docs
weight: 6200
url: /it/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

Specifica il livello di conformità agli standard PDF.

```csharp
public enum PdfCompliance
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Pdf17 | `0` | Il file di output sarà conforme allo standard PDF 1.7 (ISO 32000-1). |
| Pdf20 | `1` | Il file di output sarà conforme allo standard PDF 2.0 (ISO 32000-2). |
| PdfA1a | `2` | Il file di output sarà conforme allo standard PDF/A-1a (ISO 19005-1). Questo livello include tutti i requisiti del PDF/A-1b e richiede inoltre che la struttura del documento sia inclusa (nota anche come "taggata"), con l'obiettivo di garantire che il contenuto del documento possa essere ricercato e riutilizzato. |
| PdfA1b | `3` | Il file di output sarà conforme allo standard PDF/A-1b (ISO 19005-1). PDF/A-1b ha l'obiettivo di garantire una riproduzione affidabile dell'aspetto visivo del documento. |
| PdfA2a | `4` | Il file di output sarà conforme allo standard PDF/A-2a (ISO 19005-2). Questo livello include tutti i requisiti di PDF/A-2u e richiede inoltre che la struttura del documento sia inclusa (nota anche come "taggata"), con l'obiettivo di garantire che il contenuto del documento possa essere ricercato e riutilizzato. |
| PdfA2u | `5` | Il file di output sarà conforme allo standard PDF/A-2u (ISO 19005-2). PDF/A-2u ha l'obiettivo di preservare l'aspetto visivo statico del documento nel tempo, indipendentemente dagli strumenti e dai sistemi utilizzati per la creazione, l'archiviazione o il rendering dei file. Inoltre, qualsiasi testo contenuto nel documento può essere estratto in modo affidabile come una serie di punti di codice Unicode. |
| PdfA3a | `6` | Il file di output sarà conforme allo standard PDF/A-3a (ISO 19005-3). Questo livello include tutti i requisiti di PDF/A-3u e richiede inoltre che la struttura del documento sia inclusa (nota anche come "taggata"), con l'obiettivo di garantire che il contenuto del documento possa essere ricercato e riutilizzato. |
| PdfA3u | `7` | Il file di output sarà conforme allo standard PDF/A-3u (ISO 19005-3). PDF/A-3u (così come PDF/A-2u) ha l'obiettivo di preservare l'aspetto visivo statico del documento nel tempo, indipendentemente dagli strumenti e dai sistemi utilizzati per la creazione, l'archiviazione o il rendering dei file. Inoltre, qualsiasi testo contenuto nel documento può essere estratto in modo affidabile come una serie di punti di codice Unicode. Oltre a PDF/A-2u, PDF/A-3u consente l'incorporamento di allegati nel documento PDF. |
| PdfA4 | `8` | Il file di output sarà conforme allo standard PDF/A-4 (ISO 19005-4:2020). PDF/A-4 ha l'obiettivo di preservare l'aspetto visivo statico del documento nel tempo, indipendentemente dagli strumenti e dai sistemi utilizzati per la creazione, l'archiviazione o il rendering dei file. Inoltre, qualsiasi testo contenuto nel documento può essere estratto in modo affidabile come una serie di punti di codice Unicode. |
| PdfA4f | `9` | Il file di output sarà conforme allo standard PDF/A-4f (ISO 19005-4:2020). Questo livello include tutti i requisiti del PDF/A-4 e consente inoltre di incorporare allegati nel documento PDF. |
| PdfA4Ua2 | `10` | Il file di output sarà conforme agli standard PDF/A-4 (ISO 19005-4:2020) e PDF/UA-2 (ISO 14289-2:2024). PDF/A-4 ha l'obiettivo di preservare l'aspetto visivo statico del documento nel tempo, indipendentemente dagli strumenti e dai sistemi utilizzati per la creazione, l'archiviazione o il rendering dei file. Lo scopo principale di PDF/UA è definire come rappresentare i documenti elettronici in formato PDF in modo da renderli accessibili. |
| PdfUa1 | `11` | Il file di output sarà conforme allo standard PDF/UA-1 (ISO 14289-1). Lo scopo principale di PDF/UA è definire come rappresentare i documenti elettronici nel formato PDF in un modo che consenta l'accessibilità del file. |
| PdfUa2 | `12` | Il file di output sarà conforme allo standard PDF/UA-2 (ISO 14289-2:2024). Lo scopo principale di PDF/UA è definire come rappresentare i documenti elettronici in formato PDF in un modo che consenta l'accessibilità del file. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
