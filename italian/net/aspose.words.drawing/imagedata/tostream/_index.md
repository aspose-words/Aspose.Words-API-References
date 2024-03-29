---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words per .NET
description: ImageData ToStream metodo. Crea e restituisce uno stream che contiene i byte dellimmagine in C#.
type: docs
weight: 230
url: /it/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Crea e restituisce uno stream che contiene i byte dell'immagine.

```csharp
public Stream ToStream()
```

## Osservazioni

Se i byte dell'immagine sono archiviati nella forma, crea e restituisce aMemoryStream oggetto.

Se l'immagine è collegata e archiviata in un file, apre il file e restituisce aFileStream oggetto.

Se l'immagine è collegata e archiviata in un URL esterno, scarica il file e restituisce aMemoryStream oggetto.

È responsabilità del chiamante eliminare l'oggetto stream.

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
