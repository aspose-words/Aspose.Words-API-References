---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words per .NET
description: Scopri se una forma è un'immagine con la proprietà IsImage di ShapeBase. Identifica facilmente le forme immagine per una maggiore flessibilità e funzionalità di progettazione.
type: docs
weight: 300
url: /it/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

Restituisce`VERO` se questa forma è una forma immagine.

```csharp
public bool IsImage { get; }
```

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

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
