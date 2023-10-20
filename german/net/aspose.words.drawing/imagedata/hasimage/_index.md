---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words für .NET
description: ImageData HasImage eigendom. Gibt zurückWAHR wenn die Form Bildbytes hat oder ein Bild verknüpft in C#.
type: docs
weight: 110
url: /de/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Gibt zurück`WAHR` wenn die Form Bildbytes hat oder ein Bild verknüpft.

```csharp
public bool HasImage { get; }
```

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
