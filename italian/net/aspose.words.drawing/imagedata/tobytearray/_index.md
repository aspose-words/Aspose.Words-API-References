---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words per .NET
description: Converti qualsiasi immagine in un array di byte senza sforzo con il metodo ImageData ToByteArray. Accedi facilmente ai byte delle immagini da fonti archiviate o collegate!
type: docs
weight: 220
url: /it/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Restituisce i byte dell'immagine per qualsiasi immagine, indipendentemente dal fatto che l'immagine sia memorizzata o collegata.

```csharp
public byte[] ToByteArray()
```

## Osservazioni

Se l'immagine è collegata, scarica l'immagine ogni volta che viene richiamata.

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
