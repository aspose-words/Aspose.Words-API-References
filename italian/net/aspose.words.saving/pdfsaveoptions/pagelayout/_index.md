---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words per .NET
description: Scopri la proprietà PdfSaveOptions PageLayout per personalizzare il layout del tuo PDF e ottenere una visualizzazione ottimale su qualsiasi lettore. Migliora la presentazione del tuo documento!
type: docs
weight: 250
url: /it/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

Specifica il layout di pagina da utilizzare quando il documento viene aperto in un lettore PDF.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## Osservazioni

Il valore predefinito èSinglePage .

## Esempi

Mostra come visualizzare le pagine quando vengono aperte in un lettore PDF.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Visualizza le pagine due alla volta, con le pagine dispari a sinistra.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Guarda anche

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
