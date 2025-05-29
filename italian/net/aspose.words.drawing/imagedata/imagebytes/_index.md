---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImageBytes di ImageData per gestire e manipolare facilmente i byte delle immagini grezze all'interno delle tue forme, ottenendo contenuti visivi migliori.
type: docs
weight: 120
url: /it/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Ottiene o imposta i byte grezzi dell'immagine memorizzata nella forma.

```csharp
public byte[] ImageBytes { get; set; }
```

## Osservazioni

Impostando il valore su`null` oppure un array vuoto rimuoverà l'immagine dalla forma.

Resi`null` se l'immagine non è memorizzata nel documento (ad esempio, in questo caso l'immagine è probabilmente collegata).

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
