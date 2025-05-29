---
title: ImageData.ImageType
linktitle: ImageType
articleTitle: ImageType
second_title: .NET için Aspose.Words
description: Görüntü türlerini kolayca tanımlamak ve görüntü işleme yeteneklerinizi geliştirmek için ImageData ImageType özelliğini keşfedin. Geliştirme verimliliğinizi bugün artırın!
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

Bir belgeden resimlerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Şekil koleksiyonunu belgeden al,
// ve her şeklin görüntü verisini, görüntü içeren bir dosya olarak yerel dosya sistemine kaydeder.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Şekillerin görüntü verileri birçok olası görüntü formatındaki görüntüleri içerebilir.
        // Her bir resim için, formatına bağlı olarak otomatik olarak bir dosya uzantısı belirleyebiliriz.
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
