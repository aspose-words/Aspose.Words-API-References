---
title: ImageData.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: .NET için Aspose.Words
description: Bağlantılı görüntü yollarını ve dosya adlarını kolayca yönetmek ve görüntü işleme verimliliğinizi artırmak için ImageData SourceFullName özelliğini keşfedin.
type: docs
weight: 170
url: /tr/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Bağlantılı görüntü için kaynak dosyasının yolunu ve adını alır veya ayarlar.

```csharp
public string SourceFullName { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

Eğer`SourceFullName` boş bir dize değildir, resim bağlantılıdır.

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

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
