---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: .NET için Aspose.Words
description: ImageData'daki ToImage yönteminin gücünü açığa çıkararak şekillerde Image nesneleri olarak saklanan görüntüleri kolayca alın. Projelerinizi zahmetsizce geliştirin!
type: docs
weight: 230
url: /tr/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Şekilde depolanan görüntüyü birImage nesne.

```csharp
public Image ToImage()
```

## Notlar

Yeni birImage Bu metot her çağrıldığında nesne oluşturulur.

Resim nesnesinin imha edilmesi çağıranın sorumluluğundadır.

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
