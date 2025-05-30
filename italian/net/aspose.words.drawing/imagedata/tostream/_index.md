---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words per .NET
description: Scopri il metodo ImageData ToStream converti in modo efficiente le immagini in flussi di byte per una gestione dei dati ottimale e prestazioni applicative migliorate.
type: docs
weight: 240
url: /it/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Crea e restituisce un flusso contenente i byte dell'immagine.

```csharp
public Stream ToStream()
```

## Osservazioni

Se i byte dell'immagine sono memorizzati nella forma, crea e restituisce unMemoryStream oggetto.

Se l'immagine è collegata e memorizzata in un file, apre il file e restituisce unFileStream oggetto.

Se l'immagine è collegata e memorizzata in un URL esterno, scarica il file e restituisce unMemoryStream oggetto.

È responsabilità del chiamante eliminare l'oggetto stream.

## Esempi

Mostra come creare un file immagine dai dati immagine grezzi di una forma.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() restituisce l'array memorizzato nella proprietà ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Salva i dati dell'immagine della forma in un file immagine nel file system locale.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
