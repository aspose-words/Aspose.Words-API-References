---
title: Shape.ImageData
linktitle: ImageData
articleTitle: ImageData
second_title: .NET için Aspose.Words
description: Shape ImageData özelliğiyle şekil resimlerine zahmetsizce erişin ve yönetin. Anında sonuçlar alın veya geçerli değilse null. Tasarım iş akışınızı geliştirin!
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

Şeklin görüntüsüne erişim sağlar. Geri döndürür`hükümsüz` eğer şeklin bir görüntüsü olamazsa.

```csharp
public ImageData ImageData { get; }
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

Bağlantılı bir resmin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Aşağıda bir şeklin görüntülenebilmesi için bir resmin üzerine uygulanmasının iki yolu bulunmaktadır.
// 1 - Şekli resmi içerecek şekilde ayarlayın.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Şekilde depoladığımız her resim, belgemizin boyutunu artıracaktır.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Şekli yerel dosya sistemindeki bir resim dosyasına bağlanacak şekilde ayarlayın.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Resimlere bağlantı vermek yerden tasarruf sağlayacak ve daha küçük bir belgeyle sonuçlanacaktır.
// Ancak belge, yalnızca aşağıdaki durumlarda görüntüyü doğru şekilde görüntüleyebilir:
// resim dosyası şeklin "SourceFullName" özelliğinin işaret ettiği konumda mevcuttur.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Ayrıca bakınız

* class [ImageData](../../imagedata/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
