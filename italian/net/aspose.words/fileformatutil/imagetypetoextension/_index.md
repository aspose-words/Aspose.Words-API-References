---
title: FileFormatUtil.ImageTypeToExtension
second_title: Aspose.Words per .NET API Reference
description: FileFormatUtil metodo. Converte un valore enumerato del tipo di immagine Aspose.Words in unestensione di file. Lestensione restituita è una stringa minuscola con un punto iniziale.
type: docs
weight: 50
url: /it/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

Converte un valore enumerato del tipo di immagine Aspose.Words in un'estensione di file. L'estensione restituita è una stringa minuscola con un punto iniziale.

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Lancia quando non può convertire. |

### Esempi

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
        // Possiamo determinare automaticamente un'estensione di file per ogni immagine, in base al suo formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Guarda anche

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../fileformatutil/)
* assemblea [Aspose.Words](../../../)


