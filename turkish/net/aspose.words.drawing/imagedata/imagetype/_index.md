---
title: ImageData.ImageType
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words for .NET
description: ImageData ImageType mülk. Görüntünün türünü alır C#'da.
type: docs
weight: 140
url: /tr/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Görüntünün türünü alır.

```csharp
public ImageType ImageType { get; }
```

## Örnekler

Bir belgeden görüntülerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgedeki şekillerin koleksiyonunu alın,
// ve resim içeren her şeklin resim verilerini dosya olarak yerel dosya sistemine kaydedin.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Şekillerin görüntü verileri birçok olası görüntü formatındaki görüntüleri içerebilir.
        // Her görsel için formatına göre otomatik olarak bir dosya uzantısı belirleyebiliriz.
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
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
