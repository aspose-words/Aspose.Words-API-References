---
title: ImageData.IsLink
linktitle: IsLink
articleTitle: IsLink
second_title: .NET için Aspose.Words
description: ImageData IsLink özelliğinin SourceFullName ayarlandığında görüntüleri şekillere sorunsuz bir şekilde bağlayarak tasarımınızı nasıl geliştirdiğini keşfedin. Yaratıcılığınızı artırın!
type: docs
weight: 150
url: /tr/net/aspose.words.drawing/imagedata/islink/
---
## ImageData.IsLink property

Geri Döndürür`doğru` eğer görüntü şekle bağlıysa (ne zaman[`SourceFullName`](../sourcefullname/) belirtilmiştir).

```csharp
public bool IsLink { get; }
```

## Örnekler

Bir şeklin görüntü verilerinin nasıl düzenleneceğini gösterir.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Kaynak belgeden bir şekil içe aktar ve onu ilk paragrafa ekle.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// İçeri aktarılan şekil bir resim içeriyor. Resmin özelliklerine ve ham verilerine ImageData nesnesi aracılığıyla erişebiliriz.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Eğer bir resmin sınırları yoksa, ImageData nesnesi kenarlık rengini boş olarak tanımlayacaktır.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Bu görüntü yerel dosya sistemindeki başka bir şekle veya görüntü dosyasına bağlı değil.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// "Parlaklık" ve "Kontrast" özellikleri görüntü parlaklığını ve kontrastını tanımlar
// 0-1 ölçeğinde, varsayılan değer 0,5'tir.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Yukarıdaki parlaklık ve kontrast değerleri çok fazla beyaz içeren bir görüntü oluşturmuştur.
// ChromaKey özelliği ile şeffaflıkla değiştirilecek bir rengi (örneğin beyaz) seçebiliriz.
imageData.ChromaKey = Color.White;

// Kaynak şekli tekrar içe aktarın ve görüntüyü monokroma ayarlayın.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Üçüncü bir görüntü oluşturmak için kaynak şekli tekrar içe aktarın ve onu BiLevel olarak ayarlayın.
// BiLevel her pikseli orijinal renge en yakın olanı siyaha veya beyaza ayarlar.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Kırpma 0-1 ölçeğinde belirlenir. Bir tarafı 0,3 oranında kırpmak
// Resmin kırpılmış tarafının %30'unu kesecektir.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Ayrıca bakınız

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
