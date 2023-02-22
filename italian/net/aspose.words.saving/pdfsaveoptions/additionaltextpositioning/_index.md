---
title: PdfSaveOptions.AdditionalTextPositioning
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Un flag che specifica se scrivere o meno operatori di posizionamento del testo aggiuntivi.
type: docs
weight: 20
url: /it/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Un flag che specifica se scrivere o meno operatori di posizionamento del testo aggiuntivi.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

### Osservazioni

Se`VERO` , nel PDF di output vengono scritti ulteriori operatori di posizionamento del testo. Questo può aiutare a superare problemi con il posizionamento impreciso del testo con alcune stampanti. Lo svantaggio è l'aumento delle dimensioni del documento PDF.

Il valore predefinito è`falso`.

### Esempi

Mostra come scrivere ulteriori operatori di posizionamento del testo.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Imposta la proprietà "AdditionalTextPositioning" su "true" per tentare di correggere l'errore
    // posizionamento dell'elemento nel PDF di output, se presente, a costo di una maggiore dimensione del file.
    // Imposta la proprietà "AdditionalTextPositioning" su "false" per eseguire il rendering del documento come al solito.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


