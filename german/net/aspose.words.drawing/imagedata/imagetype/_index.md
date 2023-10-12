---
title: ImageData.ImageType
second_title: Aspose.Words für .NET-API-Referenz
description: ImageData eigendom. Ruft den Typ des Bildes ab.
type: docs
weight: 140
url: /de/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Ruft den Typ des Bildes ab.

```csharp
public ImageType ImageType { get; }
```

### Beispiele

Zeigt, wie man Bilder aus einem Dokument extrahiert und sie als einzelne Dateien im lokalen Dateisystem speichert.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Formensammlung aus dem Dokument,
// und die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem speichern.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten.
        // Wir können für jedes Bild automatisch eine Dateierweiterung anhand seines Formats ermitteln.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Siehe auch

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../imagedata/)
* Montage [Aspose.Words](../../../)


