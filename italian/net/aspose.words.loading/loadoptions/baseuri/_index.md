---
title: LoadOptions.BaseUri
second_title: Aspose.Words per .NET API Reference
description: LoadOptions proprietà. Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può esserenullo o stringa vuota. Limpostazione predefinita ènullo .
type: docs
weight: 20
url: /it/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere`nullo` o stringa vuota. L'impostazione predefinita è`nullo` .

```csharp
public string BaseUri { get; set; }
```

### Osservazioni

Questa proprietà viene utilizzata per risolvere gli URI relativi in assoluti nei seguenti casi:

1. Quando si carica un documento HTML da uno stream e il documento contiene immagini con URI relativi e non ha un URI di base specificato nell'elemento BASE HTML.
2. Quando si salva un documento in PDF e altri formati, per recuperare le immagini collegate utilizzando gli URI relativi in modo che le immagini possano essere salvate nel documento di output.

### Esempi

Mostra come aprire un documento HTML con immagini da un flusso utilizzando un URI di base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Passa l'URI della cartella base durante il caricamento
    // in modo che sia possibile trovare eventuali immagini con relativi URI nel documento HTML.
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


