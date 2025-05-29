---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words per .NET
description: Scopri come la proprietà UseSdtTagAsFormFieldName di PdfSaveOptions migliora i moduli PDF utilizzando i tag di controllo SDT per una migliore organizzazione e chiarezza.
type: docs
weight: 340
url: /it/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

Specifica se utilizzare il controllo SDT Tag o la proprietà Id come nome del campo modulo in PDF.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`.

Quando impostato su`falso`, la proprietà Id del controllo SDT viene utilizzata come nome del campo del modulo nel PDF.

Quando impostato su`VERO`, la proprietà Tag del controllo SDT viene utilizzata come nome del campo del modulo nel PDF.

Se impostato su`VERO` e il tag è vuoto, la proprietà Id verrà utilizzata come nome del campo del modulo.

Se impostato su`VERO` e i valori dei tag non sono univoci, i valori dei tag duplicati verranno modificati per creare nomi di campi del modulo PDF univoci.

## Esempi

Mostra come utilizzare il controllo SDT Tag o la proprietà Id come nome del campo modulo in PDF.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// Se impostata su 'false', la proprietà Id del controllo SDT viene utilizzata come nome del campo del modulo nel PDF.
// Se impostata su 'true', la proprietà Tag del controllo SDT viene utilizzata come nome del campo del modulo nel PDF.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
