---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words per .NET
description: Scopri la proprietà AdditionalTextPositioning di PdfSaveOptions per controllare il posizionamento del testo nei PDF. Migliora il layout del tuo documento senza sforzo!
type: docs
weight: 20
url: /it/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Un flag che specifica se scrivere o meno operatori di posizionamento del testo aggiuntivi.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Osservazioni

Se`VERO` , vengono scritti ulteriori operatori di posizionamento del testo nel PDF di output. Questo potrebbe aiutare a superare i problemi di posizionamento impreciso del testo con alcune stampanti. Lo svantaggio è l'aumento delle dimensioni del documento PDF.

Il valore predefinito è`falso`.

## Esempi

Mostra come scrivere ulteriori operatori di posizionamento del testo.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Imposta la proprietà "AdditionalTextPositioning" su "true" per tentare di correggere errori
    // posizionamento degli elementi nel PDF di output, se presenti, a scapito dell'aumento delle dimensioni del file.
    // Impostare la proprietà "AdditionalTextPositioning" su "false" per visualizzare il documento come di consueto.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
