---
title: ImageData.ToImage
second_title: Aspose.Words for .NET API Referansı
description: ImageData yöntem. Şekilde saklanan görüntüyü bir dosya olarak alır.Image nesne.
type: docs
weight: 230
url: /tr/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Şekilde saklanan görüntüyü bir dosya olarak alır.Image nesne.

```csharp
public Image ToImage()
```

### Notlar

Yeni birImage Bu yöntem her çağrıldığında nesne oluşturulur.

Görüntü nesnesinin imha edilmesi arayanın sorumluluğundadır.

### Örnekler

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
* ad alanı [Aspose.Words.Drawing](../../imagedata/)
* toplantı [Aspose.Words](../../../)


