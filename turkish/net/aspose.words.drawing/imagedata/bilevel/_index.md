---
title: BiLevel
second_title: Aspose.Words for .NET API Referansı
description: Bir görüntünün siyah beyaz gösterilip gösterilmeyeceğini belirler.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/imagedata/bilevel/
---
## ImageData.BiLevel property

Bir görüntünün siyah beyaz gösterilip gösterilmeyeceğini belirler.

```csharp
public bool BiLevel { get; set; }
```

### Notlar

Varsayılan değer **yanlış**.

### Örnekler

Bir şeklin görüntü verilerinin nasıl düzenleneceğini gösterir.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Kaynak belgeden bir şekil alın ve ilk paragrafa ekleyin.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// İçe aktarılan şekil bir görüntü içeriyor. ImageData nesnesi aracılığıyla görüntünün özelliklerine ve ham verilerine erişebiliriz.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Bir görüntünün sınırları yoksa, ImageData nesnesi kenarlık rengini boş olarak tanımlar.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Bu görüntü, yerel dosya sistemindeki başka bir şekle veya görüntü dosyasına bağlanmıyor.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// "Parlaklık" ve "Kontrast" özellikleri, görüntünün parlaklığını ve kontrastını tanımlar
// 0-1 ölçeğinde, varsayılan değer 0,5'tir.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Yukarıdaki parlaklık ve kontrast değerleri, beyazın bol olduğu bir görüntü oluşturmuştur.
// Beyaz gibi şeffaflık ile değiştirmek için ChromaKey özelliği ile bir renk seçebiliriz.
imageData.ChromaKey = Color.White;

// Kaynak şekli tekrar içe aktarın ve görüntüyü monokrom olarak ayarlayın.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Üçüncü bir görüntü oluşturmak için kaynak şekli tekrar içe aktarın ve BiLevel'e ayarlayın.
// BiLevel, her pikseli siyah veya beyaza (hangisi orijinal renge daha yakınsa) ayarlar.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Kırpma 0-1 ölçeğinde belirlenir. Bir tarafı 0,3 ile kırpma
// görüntünün %30'unu kırpılan taraftan kırpacak.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Ayrıca bakınız

* class [ImageData](../../imagedata)
* ad alanı [Aspose.Words.Drawing](../../imagedata)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->