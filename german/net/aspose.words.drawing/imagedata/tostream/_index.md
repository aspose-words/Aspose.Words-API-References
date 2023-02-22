---
title: ImageData.ToStream
second_title: Aspose.Words für .NET-API-Referenz
description: ImageData methode. Erstellt und gibt einen Stream zurück der die Bildbytes enthält.
type: docs
weight: 230
url: /de/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Erstellt und gibt einen Stream zurück, der die Bildbytes enthält.

```csharp
public Stream ToStream()
```

### Bemerkungen

Wenn die Bildbytes in der Form gespeichert sind, wird a erstellt und zurückgegebenMemoryStream Objekt.

Wenn das Bild verknüpft und in einer Datei gespeichert ist, öffnet die Datei und gibt a zurückFileStream Objekt.

Wenn das Bild verknüpft und in einer externen URL gespeichert ist, lädt die Datei herunter und gibt a zurückMemoryStream Objekt.

Liegt es in der Verantwortung des Aufrufers, das Stream-Objekt zu entsorgen?

### Beispiele

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
* namensraum [Aspose.Words.Drawing](../../imagedata/)
* Montage [Aspose.Words](../../../)


