---
title: ImageData.ImageType
second_title: Aspose.Words for .NET API Referansı
description: ImageData mülk. Resmin türünü alır.
type: docs
weight: 140
url: /tr/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Resmin türünü alır.

```csharp
public ImageType ImageType { get; }
```

### Örnekler

Bir belgeden görüntülerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgeden şekil koleksiyonunu alın,
// ve bir görüntü ile her şeklin görüntü verilerini yerel dosya sistemine dosya olarak kaydedin.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Şekillerin görüntü verileri, birçok olası görüntü formatının görüntülerini içerebilir. 
        // Her resim için formatına göre otomatik olarak bir dosya uzantısı belirleyebiliriz.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Ayrıca bakınız

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../imagedata/)
* toplantı [Aspose.Words](../../../)


