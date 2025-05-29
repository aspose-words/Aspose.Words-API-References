---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words für .NET
description: Nutzen Sie die Leistungsfähigkeit der ToImage-Methode in ImageData, um in Formen gespeicherte Bilder einfach als Bildobjekte abzurufen. Optimieren Sie Ihre Projekte mühelos!
type: docs
weight: 230
url: /de/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Ruft das in der Form gespeicherte Bild alsImage Objekt.

```csharp
public Image ToImage()
```

## Bemerkungen

Ein neuesImage Bei jedem Aufruf dieser Methode wird ein Objekt erstellt.

Es liegt in der Verantwortung des Anrufers, das Bildobjekt zu entsorgen.

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
