---
title: ImageData.ToImage
second_title: Aspose.Words per .NET API Reference
description: ImageData metodo. Ottiene limmagine memorizzata nella forma come aImage oggetto.
type: docs
weight: 230
url: /it/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Ottiene l'immagine memorizzata nella forma come aImage oggetto.

```csharp
public Image ToImage()
```

### Osservazioni

Un nuovoImage L'oggetto viene creato ogni volta che viene chiamato questo metodo.

È responsabilità del chiamante eliminare l'oggetto immagine.

### Esempi

Mostra come salvare tutte le immagini da un documento al file system.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Le forme con il flag impostato "HasImage" memorizzano e visualizzano tutte le immagini del documento.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// Passa attraverso ogni forma e salva la sua immagine.
ImageFormatConverter formatConverter = new ImageFormatConverter();

using (IEnumerator<Shape> enumerator = shapesWithImages.GetEnumerator())
{
    int shapeIndex = 0;

    while (enumerator.MoveNext())
    {
        ImageData imageData = enumerator.Current.ImageData;
        ImageFormat format = imageData.ToImage().RawFormat;
        string fileExtension = formatConverter.ConvertToString(format);

        using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{++shapeIndex}.{fileExtension}"))
            imageData.Save(fileStream);
    }
}
```

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../imagedata/)
* assemblea [Aspose.Words](../../../)


