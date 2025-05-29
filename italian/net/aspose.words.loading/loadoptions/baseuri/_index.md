---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words per .NET
description: Scopri la proprietà BaseUri di LoadOptions per convertire facilmente gli URI relativi in assoluti nei tuoi documenti. Migliora la tua gestione degli URI oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere`null` o stringa vuota. Il valore predefinito è`null` .

```csharp
public string BaseUri { get; set; }
```

## Osservazioni

Questa proprietà viene utilizzata per risolvere gli URI relativi in assoluti nei seguenti casi:

1. Quando si carica un documento HTML da un flusso e il documento contiene immagini con URI relativi e non ha un URI di base specificato nell'elemento BASE HTML.
2. Quando si salva un documento in formato PDF e altri formati, recuperare le immagini collegate utilizzando gli URI relativi in modo che le immagini possano essere salvate nel documento di output.

## Esempi

Mostra come aprire un documento HTML con immagini da un flusso utilizzando un URI di base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Passare l'URI della cartella base durante il caricamento
    // in modo che sia possibile trovare tutte le immagini con URI relativi nel documento HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifica che la prima forma del documento contenga un'immagine valida.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
