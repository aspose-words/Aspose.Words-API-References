---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words für .NET
description: ImageData ToByteArray methode. Gibt Bildbytes für jedes Bild zurück unabhängig davon ob das Bild gespeichert oder verknüpft ist in C#.
type: docs
weight: 210
url: /de/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild gespeichert oder verknüpft ist.

```csharp
public byte[] ToByteArray()
```

## Bemerkungen

Wenn das Bild verlinkt ist, wird das Bild bei jedem Aufruf heruntergeladen.

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
