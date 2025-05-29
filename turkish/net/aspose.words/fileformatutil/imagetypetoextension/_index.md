---
title: FileFormatUtil.ImageTypeToExtension
linktitle: ImageTypeToExtension
articleTitle: ImageTypeToExtension
second_title: .NET için Aspose.Words
description: Aspose.Words resim türlerini FileFormatUtil yöntemiyle zahmetsizce dosya uzantılarına dönüştürün. Saniyeler içinde doğru, küçük harfli uzantılar elde edin!
type: docs
weight: 50
url: /tr/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

Aspose.Words görüntü türünde numaralandırılmış bir değeri dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir.

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | Dönüştürülemediğinde atar. |

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

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
