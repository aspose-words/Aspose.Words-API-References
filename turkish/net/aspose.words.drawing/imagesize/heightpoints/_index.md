---
title: ImageSize.HeightPoints
linktitle: HeightPoints
articleTitle: HeightPoints
second_title: .NET için Aspose.Words
description: Görüntü yüksekliğini noktalar halinde kolayca almak için ImageSize HeightPoints özelliğini keşfedin; 1 nokta 1/72 inç'e eşittir. Görüntülerinizi zahmetsizce optimize edin!
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/imagesize/heightpoints/
---
## ImageSize.HeightPoints property

Resmin yüksekliğini nokta cinsinden alır. 1 nokta 1/72 inçtir.

```csharp
public double HeightPoints { get; }
```

## Örnekler

Bir şeklin resimle nasıl yeniden boyutlandırılacağını gösterir.

```csharp
// "InsertImage" metodunu kullanarak bir resim eklediğimizde, oluşturucu resmi görüntüleyen şekli şu şekilde ölçekler:
// Microsoft Word'de belgeyi %100 yakınlaştırma kullanarak görüntülediğimizde, şekil görüntüyü gerçek boyutunda görüntüler.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// 400x400 boyutundaki bir resim, 300x300pt boyutunda bir ImageData nesnesi oluşturacaktır.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Bir şeklin boyutları görüntü verilerinin boyutlarıyla eşleşiyorsa,
// daha sonra şekil, görüntüyü orijinal boyutunda görüntüler.
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

 // Şeklin genel boyutunu %50 oranında küçült.
shape.Width *= 0.5;

 // Şeklin oranlarını korumak için ölçekleme faktörleri hem genişliğe hem de yüksekliğe aynı anda uygulanır.
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// Şekli yeniden boyutlandırdığımızda resim verisinin boyutu aynı kalır.
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Görüntünün boyutuna göre ölçekleme uygulamak için görüntü veri boyutlarına başvurabiliriz.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Ayrıca bakınız

* class [ImageSize](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
