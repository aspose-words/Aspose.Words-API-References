---
title: LoadOptions.BaseUri
second_title: Aspose.Words per .NET API Reference
description: LoadOptions proprietà. Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere una stringa nulla o vuota. Il valore predefinito è null.
type: docs
weight: 20
url: /it/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere una stringa nulla o vuota. Il valore predefinito è null.

```csharp
public string BaseUri { get; set; }
```

### Osservazioni

Questa proprietà viene utilizzata per risolvere gli URI relativi in assoluto nei seguenti casi:

1. Quando si carica un documento HTML da un flusso e il documento contiene immagini con URI relativi e non ha un URI di base specificato nell'elemento BASE HTML.
2. Quando si salva un documento in PDF e altri formati, per recuperare le immagini collegate utilizzando i relativi URI in modo che le immagini possano essere salvate nel documento di output.

### Esempi

Mostra come aprire un documento HTML con immagini da un flusso usando un URI di base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Passa l'URI della cartella di base durante il caricamento
    // in modo da poter trovare qualsiasi immagine con relativi URI nel documento HTML.
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
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)


