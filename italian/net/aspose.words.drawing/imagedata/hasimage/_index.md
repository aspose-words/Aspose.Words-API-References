---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words per .NET
description: ImageData HasImage proprietà. RestituisceVERO se la forma ha byte di immagine o collega unimmagine in C#.
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
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
