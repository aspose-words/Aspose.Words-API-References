---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageData HasImage-Eigenschaft. Überprüfen Sie schnell, ob eine Form Bildbytes oder Links enthält, und verbessern Sie so mühelos Ihren Design-Workflow.
type: docs
weight: 110
url: /de/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Rückgaben`WAHR` wenn die Form Bildbytes enthält oder ein Bild verlinkt.

```csharp
public bool HasImage { get; }
```

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
