---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words per .NET
description: Scopri come la proprietà RenderChoiceFormFieldBorder di PdfSaveOptions migliora la progettazione dei moduli PDF controllando i bordi dei campi di scelta per una migliore esperienza utente.
type: docs
weight: 290
url: /it/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

Specifica se visualizzare il bordo del campo del modulo di scelta PDF.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## Osservazioni

I campi del modulo di scelta PDF vengono utilizzati per l'esportazione del controllo del contenuto della casella combinata SDT, del controllo Content dell'elenco a discesa SDT e del campo del modulo a discesa legacy quando[`PreserveFormFields`](../preserveformfields/) l'opzione è abilitata.

Il valore predefinito è`VERO`.

## Esempi

Mostra come visualizzare il bordo del campo del modulo di scelta PDF.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
