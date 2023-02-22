---
title: FileFormatUtil.ImageTypeToExtension
second_title: Aspose.Words für .NET-API-Referenz
description: FileFormatUtil methode. Konvertiert einen Aufzählungswert des Bildtyps Aspose.Words in eine Dateierweiterung. Die zurückgegebene Erweiterung ist eine Zeichenfolge in Kleinbuchstaben mit einem führenden Punkt.
type: docs
weight: 50
url: /de/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

Konvertiert einen Aufzählungswert des Bildtyps Aspose.Words in eine Dateierweiterung. Die zurückgegebene Erweiterung ist eine Zeichenfolge in Kleinbuchstaben mit einem führenden Punkt.

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Wirft, wenn nicht konvertiert werden kann. |

### Beispiele

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Sammlung von Formen aus dem Dokument,
// und die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem speichern.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten. 
        // Wir können für jedes Bild automatisch eine Dateierweiterung basierend auf seinem Format bestimmen.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Siehe auch

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../fileformatutil/)
* Montage [Aspose.Words](../../../)


