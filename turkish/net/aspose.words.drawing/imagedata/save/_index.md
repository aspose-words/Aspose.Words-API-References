---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: .NET için Aspose.Words
description: ImageData Save yöntemiyle görüntüleri zahmetsizce kaydedin. Görüntüleri doğrudan seçtiğiniz akışa kolayca depolayarak iş akışınızı kolaylaştırın.
type: docs
weight: 200
url: /tr/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

Görüntüyü belirtilen akışa kaydeder.

```csharp
public void Save(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Resmin kaydedileceği akış. |

## Notlar

Akış nesnesini elden çıkarmak çağıranın sorumluluğunda mıdır?

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

---

## Save(*string*) {#save_1}

Görüntüyü bir dosyaya kaydeder.

```csharp
public void Save(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resmin kaydedileceği dosya adı. |

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

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
