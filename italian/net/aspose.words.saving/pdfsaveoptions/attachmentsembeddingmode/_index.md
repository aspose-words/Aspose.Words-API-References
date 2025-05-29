---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: Aspose.Words per .NET
description: Personalizza il modo in cui gli allegati vengono incorporati nei PDF con PdfSaveOptions. Garantisci un'integrazione perfetta e una condivisione ottimizzata dei documenti.
type: docs
weight: 30
url: /it/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

Ottiene o imposta un valore che determina come gli allegati vengono incorporati nel documento PDF.

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## Osservazioni

Il valore predefinito èNone e gli allegati non sono incorporati.

Gli standard PDF/A-1, PDF/A-2 e PDF/A-4 standard (non PDF/A-4f) non consentono file incorporati. None il valore verrà utilizzato automaticamente.

## Esempi

Mostra come aggiungere allegati incorporati al documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### Guarda anche

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
