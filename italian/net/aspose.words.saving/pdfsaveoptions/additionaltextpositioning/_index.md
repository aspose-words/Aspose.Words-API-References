---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words per .NET
description: PdfSaveOptions AdditionalTextPositioning proprietà. Un flag che specifica se scrivere o meno operatori di posizionamento del testo aggiuntivi in C#.
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

Se`VERO` , ulteriori operatori di posizionamento del testo vengono scritti nel PDF di output. Ciò può aiutare a superare i problemi relativi al posizionamento impreciso del testo con alcune stampanti. Lo svantaggio è l'aumento delle dimensioni del documento PDF.

Il valore predefinito è`falso`.

## Esempi

Mostra come scrivere ulteriori operatori di posizionamento del testo.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Imposta la proprietà "AdditionalTextPositioning" su "true" per tentare di correggere l'errore
    // posizionamento degli elementi nel PDF di output, qualora ce ne fossero, al costo di un aumento delle dimensioni del file.
    // Imposta la proprietà "AdditionalTextPositioning" su "false" per visualizzare il documento come al solito.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
