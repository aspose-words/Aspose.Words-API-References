---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageData ImageBytes-Eigenschaft, um Rohbildbytes in Ihren Formen einfach zu verwalten und zu bearbeiten und so den visuellen Inhalt zu verbessern.
type: docs
weight: 120
url: /de/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Ruft die Rohbytes des in der Form gespeicherten Bildes ab oder legt sie fest.

```csharp
public byte[] ImageBytes { get; set; }
```

## Bemerkungen

Setzen Sie den Wert auf`null` oder ein leeres Array entfernt das Bild aus der Form.

Rückgaben`null` wenn das Bild nicht im Dokument gespeichert ist (z. B. ist das Bild in diesem Fall wahrscheinlich verknüpft).

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
