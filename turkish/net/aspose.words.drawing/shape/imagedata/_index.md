---
title: Shape.ImageData
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words for .NET
description: Shape ImageData mülk. Şeklin görüntüsüne erişim sağlar. Döndürürhükümsüz şeklin bir resmi olamazsa C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

Şeklin görüntüsüne erişim sağlar. Döndürür`hükümsüz` şeklin bir resmi olamazsa.

```csharp
public ImageData ImageData { get; }
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

Bağlantılı bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Aşağıda, bir şekli görüntüleyebilmesi için bir şekle uygulamanın iki yolu verilmiştir.
// 1 - Resmi içerecek şekli ayarlayın.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Şekilde sakladığımız her görsel belgemizin boyutunu artıracaktır.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Yerel dosya sistemindeki bir görüntü dosyasına bağlanacak şekli ayarlayın.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Resimlere bağlantı verilmesi yerden tasarruf sağlar ve belgenin daha küçük olmasını sağlar.
// Ancak belge görüntüyü yalnızca doğru şekilde görüntüleyebilir
// görüntü dosyası, şeklin "SourceFullName" özelliğinin işaret ettiği konumda mevcut.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Ayrıca bakınız

* class [ImageData](../../imagedata/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
