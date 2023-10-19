---
title: ImageData.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words for .NET
description: ImageData SourceFullName mülk. Bağlı görüntünün kaynak dosyasının yolunu ve adını alır veya ayarlar C#'da.
type: docs
weight: 170
url: /tr/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Bağlı görüntünün kaynak dosyasının yolunu ve adını alır veya ayarlar.

```csharp
public string SourceFullName { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

Eğer`SourceFullName` boş bir dize değil, görüntü bağlantılı.

## Örnekler

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

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
