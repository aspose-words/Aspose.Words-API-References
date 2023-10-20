---
title: ImageData.IsLinkOnly
linktitle: IsLinkOnly
articleTitle: IsLinkOnly
second_title: Aspose.Words for .NET
description: ImageData IsLinkOnly mülk. İadelerdoğru resim bağlantılıysa ve belgede saklanmıyorsa C#'da.
type: docs
weight: 160
url: /tr/net/aspose.words.drawing/imagedata/islinkonly/
---
## ImageData.IsLinkOnly property

İadeler`doğru` resim bağlantılıysa ve belgede saklanmıyorsa.

```csharp
public bool IsLinkOnly { get; }
```

## Örnekler

Bir şeklin görüntü verilerinin nasıl düzenleneceğini gösterir.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Kaynak belgeden bir şekil içe aktarın ve onu ilk paragrafa ekleyin.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// İçe aktarılan şekil bir resim içeriyor. ImageData nesnesi aracılığıyla görüntünün özelliklerine ve ham verilerine erişebiliriz.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Bir görüntünün kenarlıkları yoksa, ImageData nesnesi kenarlık rengini boş olarak tanımlayacaktır.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Bu görüntü, yerel dosya sistemindeki başka bir şekil veya görüntü dosyasına bağlanmaz.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// "Parlaklık" ve "Kontrast" özellikleri görüntünün parlaklığını ve kontrastını tanımlar
// 0-1 ölçeğinde, varsayılan değer 0,5'tir.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Yukarıdaki parlaklık ve kontrast değerleri beyazın bol olduğu bir görüntü oluşturdu.
// ChromaKey özelliği ile şeffaflıkla değiştirilecek beyaz gibi bir renk seçebiliriz.
imageData.ChromaKey = Color.White;

// Kaynak şekli tekrar içe aktarın ve görüntüyü tek renkli olarak ayarlayın.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Üçüncü bir görüntü oluşturmak için kaynak şekli tekrar içe aktarın ve BiLevel'e ayarlayın.
// BiLevel her pikseli siyah veya beyaza (hangisi orijinal renge daha yakınsa) ayarlar.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Kırpma 0-1 ölçeğinde belirlenir. Bir tarafı 0,3 oranında kırpma
// kırpılan taraftaki görüntünün %30'unu kırpacaktır.
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
