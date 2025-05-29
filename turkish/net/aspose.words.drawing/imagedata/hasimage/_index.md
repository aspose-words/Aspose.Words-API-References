---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: .NET için Aspose.Words
description: ImageData HasImage özelliğini keşfedin. Bir şeklin resim baytları veya bağlantılar içerip içermediğini hızlıca kontrol edin, tasarım iş akışınızı zahmetsizce geliştirin.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Geri Döndürür`doğru` eğer şeklin görüntü baytları varsa veya bir görüntüye bağlantı veriyorsa.

```csharp
public bool HasImage { get; }
```

## Örnekler

Bir belgedeki tüm resimlerin dosya sistemine nasıl kaydedileceğini gösterir.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// "HasImage" bayrağı ayarlanmış şekiller belgenin tüm resimlerini saklar ve görüntüler.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Her şeklin üzerinden geçin ve resmini kaydedin.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Ayrıca bakınız

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
