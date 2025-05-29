---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageData-ToStream-Methode – konvertieren Sie Bilder effizient in Byte-Streams für eine nahtlose Datenverarbeitung und verbesserte Anwendungsleistung.
type: docs
weight: 240
url: /de/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Erstellt und gibt einen Stream zurück, der die Bildbytes enthält.

```csharp
public Stream ToStream()
```

## Bemerkungen

Wenn die Bildbytes in der Form gespeichert sind, erstellt und gibt einMemoryStream Objekt.

Wenn das Bild verknüpft und in einer Datei gespeichert ist, öffnet die Datei und gibt eineFileStream Objekt.

Wenn das Bild verlinkt und in einer externen URL gespeichert ist, lädt die Datei herunter und gibt eineMemoryStream Objekt.

Liegt es in der Verantwortung des Anrufers, das Stream-Objekt zu entsorgen?

## Beispiele

Zeigt, wie aus den Rohbilddaten einer Form eine Bilddatei erstellt wird.

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
