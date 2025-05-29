---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImageData HasImage. Controlla rapidamente se una forma contiene byte o link di immagini, migliorando il tuo flusso di lavoro di progettazione senza sforzo.
type: docs
weight: 110
url: /it/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Restituisce`VERO` se la forma ha byte di immagine o collega un'immagine.

```csharp
public bool HasImage { get; }
```

## Esempi

Mostra come salvare tutte le immagini da un documento al file system.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Le forme con il flag "HasImage" impostato memorizzano e visualizzano tutte le immagini del documento.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Esamina ogni forma e salva la relativa immagine.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
