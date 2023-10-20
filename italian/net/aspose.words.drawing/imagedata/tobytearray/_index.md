---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words per .NET
description: ImageData ToByteArray metodo. Restituisce byte immagine per qualsiasi immagine indipendentemente dal fatto che limmagine sia archiviata o collegata in C#.
type: docs
weight: 210
url: /it/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Restituisce byte immagine per qualsiasi immagine indipendentemente dal fatto che l'immagine sia archiviata o collegata.

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

// ToByteArray() restituisce l'array archiviato nella proprietà ImageBytes.
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
