---
title: ImageData.ImageBytes
second_title: Aspose.Words für .NET-API-Referenz
description: ImageData eigendom. Ruft die Rohbytes des in der Form gespeicherten Bildes ab oder legt diese fest.
type: docs
weight: 120
url: /de/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Ruft die Rohbytes des in der Form gespeicherten Bildes ab oder legt diese fest.

```csharp
public byte[] ImageBytes { get; set; }
```

### Bemerkungen

Den Wert auf setzen`Null` oder ein leeres Array entfernt das Bild aus der Form.

Kehrt zurück`Null` wenn das Bild nicht im Dokument gespeichert ist (z. B. ist das Bild in diesem Fall wahrscheinlich verlinkt).

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


