---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words für .NET
description: ImageData ToStream methode. Erstellt einen Stream der die Bildbytes enthält und gibt ihn zurück in C#.
type: docs
weight: 230
url: /de/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Erstellt einen Stream, der die Bildbytes enthält, und gibt ihn zurück.

```csharp
public Stream ToStream()
```

## Bemerkungen

Wenn die Bildbytes in der Form gespeichert sind, wird eine erstellt und zurückgegebenMemoryStream Objekt.

Wenn das Bild verknüpft und in einer Datei gespeichert ist, wird die Datei geöffnet und eine zurückgegebenFileStream Objekt.

Wenn das Bild verlinkt und in einer externen URL gespeichert ist, wird die Datei heruntergeladen und eine zurückgegebenMemoryStream Objekt.

Liegt es in der Verantwortung des Aufrufers, das Stream-Objekt zu entsorgen?

## Beispiele

Zeigt, wie eine Bilddatei aus den Rohbilddaten einer Form erstellt wird.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() gibt das in der ImageBytes-Eigenschaft gespeicherte Array zurück.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Speichern Sie die Bilddaten der Form in einer Bilddatei im lokalen Dateisystem.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### Siehe auch

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
