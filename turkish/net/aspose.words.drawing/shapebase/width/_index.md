---
title: ShapeBase.Width
linktitle: Width
articleTitle: Width
second_title: .NET için Aspose.Words
description: ShapeBase Width özelliğini keşfedin. Gelişmiş tasarım esnekliği ve hassasiyeti için şeklinizin içeren bloğunun genişliğini kolayca ayarlayın.
type: docs
weight: 610
url: /tr/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Şeklin içeren bloğunun genişliğini alır veya ayarlar.

```csharp
public double Width { get; set; }
```

## Notlar

En üst düzey bir şekil için değer puan cinsindendir.

Bir gruptaki şekiller için değer, üst grubun koordinat alanında ve birimlerindedir.

Varsayılan değer 0'dır.

## Örnekler

Kayan bir resmin nasıl ekleneceğini, konumunun ve boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Şeklin "RelativeHorizontalPosition" özelliğini "Left" özelliğinin değerini işleyecek şekilde yapılandırın
 // şeklin sayfanın sol tarafından yatay uzaklığı, nokta cinsinden.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Şeklin sayfanın sol tarafından yatay uzaklığını 100 olarak ayarlayın.
shape.Left = 100;

// Şekli sayfanın üstünden 80pt aşağıya yerleştirmek için benzer şekilde "RelativeVerticalPosition" özelliğini kullanın.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Şeklin yüksekliğini ayarlayın, bu sayede boyutlar korunarak genişlik otomatik olarak ölçeklenir.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// "Alt" ve "Sağ" özellikleri, görüntünün alt ve sağ kenarlarını içerir.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

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

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
