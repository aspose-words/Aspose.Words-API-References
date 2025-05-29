---
title: Shape.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words per .NET
description: Scopri se una forma contiene dati immagine o collegamenti a un'immagine con la proprietà HasImage. Migliora i tuoi progetti senza sforzo!
type: docs
weight: 90
url: /it/net/aspose.words.drawing/shape/hasimage/
---
## Shape.HasImage property

Restituisce`VERO` se la forma ha byte di immagine o collega un'immagine.

```csharp
public bool HasImage { get; }
```

## Esempi

Mostra come eliminare tutte le forme con immagini da un documento.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Mostra come estrarre immagini da un documento e salvarle nel file system locale come file singoli.

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
         // I dati immagine delle forme possono contenere immagini di molti possibili formati.
        // Possiamo determinare automaticamente un'estensione di file per ogni immagine, in base al suo formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Guarda anche

* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
