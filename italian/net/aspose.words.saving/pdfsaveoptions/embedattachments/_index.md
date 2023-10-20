---
title: PdfSaveOptions.EmbedAttachments
linktitle: EmbedAttachments
articleTitle: EmbedAttachments
second_title: Aspose.Words per .NET
description: PdfSaveOptions EmbedAttachments proprietà. Ottiene o imposta un valore che determina se incorporare o meno gli allegati nel documento PDF in C#.
type: docs
weight: 110
url: /it/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

Ottiene o imposta un valore che determina se incorporare o meno gli allegati nel documento PDF.

```csharp
public bool EmbedAttachments { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` gli allegati non sono incorporati.

Quando il valore è`VERO` gli allegati vengono incorporati nel documento PDF.

L'incorporamento degli allegati non è supportato durante il salvataggio in conformità PDF/A e PDF/UA. `falso` il valore verrà utilizzato automaticamente.

L'incorporamento degli allegati non è supportato quando la crittografia è abilitata.`falso` value verrà utilizzato automaticamente.

## Esempi

Mostra come aggiungere allegati incorporati al documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
