---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words for .NET
description: ImageData HasImage mülk. İadelerdoğru şeklin görüntü baytları varsa veya bir görüntüye bağlantı veriyorsa C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

İadeler`doğru` şeklin görüntü baytları varsa veya bir görüntüye bağlantı veriyorsa.

```csharp
public bool HasImage { get; }
```

## Örnekler

Bir belgedeki tüm görüntülerin dosya sistemine nasıl kaydedileceğini gösterir.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// "HasImage" bayrak setine sahip şekiller belgenin tüm resimlerini saklar ve görüntüler.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// Her şeklin üzerinden geçin ve görüntüsünü kaydedin.
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

### Ayrıca bakınız

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
