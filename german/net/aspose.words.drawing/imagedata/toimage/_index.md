---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words für .NET
description: ImageData ToImage methode. Ruft das in der Form gespeicherte Bild als abImage Objekt in C#.
type: docs
weight: 220
url: /de/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Ruft das in der Form gespeicherte Bild als abImage Objekt.

```csharp
public Image ToImage()
```

## Bemerkungen

Ein neuerImage Das Objekt wird bei jedem Aufruf dieser Methode erstellt.

Es liegt in der Verantwortung des Aufrufers, über das Bildobjekt zu verfügen.

## Beispiele

Zeigt, wie alle Bilder eines Dokuments im Dateisystem gespeichert werden.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Formen mit gesetztem „HasImage“-Flag speichern und zeigen alle Bilder des Dokuments an.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// Jede Form durchgehen und ihr Bild speichern.
ImageFormatConverter formatConverter = new ImageFormatConverter();

using (IEnumerator<Shape> enumerator = shapesWithImages.GetEnumerator())
{
    int shapeIndex = 0;

    while (enumerator.MoveNext())
    {
        ImageData imageData = enumerator.Current.ImageData;
        ImageFormat format = imageData.ToImage().RawFormat;
        string fileExtension = formatConverter.ConvertToString(format);

        using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{++shapeIndex}.{fileExtension}"))
            imageData.Save(fileStream);
    }
}
```

### Siehe auch

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
