---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words für .NET
description: Speichern Sie Bilder mühelos mit der ImageData-Speichermethode. Optimieren Sie Ihren Workflow, indem Sie Bilder direkt im gewünschten Stream speichern.
type: docs
weight: 200
url: /de/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

Speichert das Bild im angegebenen Stream.

```csharp
public void Save(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, in dem das Bild gespeichert werden soll. |

## Bemerkungen

Liegt es in der Verantwortung des Anrufers, das Stream-Objekt zu entsorgen?

## Beispiele

Zeigt, wie alle Bilder aus einem Dokument im Dateisystem gespeichert werden.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Formen mit gesetztem „HasImage“-Flag speichern und zeigen alle Bilder des Dokuments an.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Gehen Sie jede Form durch und speichern Sie ihr Bild.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Siehe auch

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

Speichert das Bild in einer Datei.

```csharp
public void Save(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Dateiname, unter dem das Bild gespeichert werden soll. |

## Beispiele

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Sammlung von Formen aus dem Dokument,
// und speichere die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem.
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

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
