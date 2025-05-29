---
title: DocumentBuilder.InsertNode
linktitle: InsertNode
articleTitle: InsertNode
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertNode yöntemiyle belge oluşturmanızı geliştirin. Sorunsuz düzenleme için imlecin önüne düğümleri zahmetsizce ekleyin!
type: docs
weight: 410
url: /tr/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

İmlecin önüne bir düğüm ekler.

```csharp
public void InsertNode(Node node)
```

## Örnekler

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
