---
title: ImageData.ImageType
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words per .NET
description: ImageData ImageType proprietà. Ottiene il tipo di immagine in C#.
type: docs
weight: 140
url: /it/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Ottiene il tipo di immagine.

```csharp
public ImageType ImageType { get; }
```

## Esempi

Mostra come estrarre immagini da un documento e salvarle nel file system locale come singoli file.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Ottieni la raccolta di forme dal documento,
// e salva i dati dell'immagine di ogni forma con un'immagine come file nel file system locale.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // I dati immagine delle forme possono contenere immagini di molti possibili formati immagine.
        // Possiamo determinare automaticamente un'estensione di file per ciascuna immagine, in base al suo formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Guarda anche

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
