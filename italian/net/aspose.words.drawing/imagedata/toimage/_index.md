---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words per .NET
description: Sfrutta la potenza del metodo ToImage in ImageData per recuperare facilmente le immagini memorizzate nelle forme come oggetti Immagine. Migliora i tuoi progetti senza sforzo!
type: docs
weight: 230
url: /it/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Ottiene l'immagine memorizzata nella forma comeImage oggetto.

```csharp
public Image ToImage()
```

## Osservazioni

Un nuovoImage L'oggetto viene creato ogni volta che viene chiamato questo metodo.

È responsabilità del chiamante eliminare l'oggetto immagine.

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
