---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: .NET için Aspose.Words
description: Gelişmiş belge kalitesi için ayrıntılı görüntü boyutu ve çözünürlük bilgilerine ulaşabileceğiniz kaynak olan Aspose.Words.Drawing.ImageSize sınıfını keşfedin.
type: docs
weight: 1400
url: /tr/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Görüntü boyutu ve çözünürlüğü hakkında bilgi içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Görüntülerle Çalışma](https://docs.aspose.com/words/net/working-with-images/) belgeleme makalesi.

```csharp
public class ImageSize
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ImageSize](imagesize/#constructor)(*int, int*) | Genişliği ve yüksekliği piksel cinsinden verilen değerlere başlatır. Çözünürlüğü 96 dpi'ye başlatır. |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | Genişliği, yüksekliği ve çözünürlüğü verilen değerlere göre başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | Görüntünün yüksekliğini piksel cinsinden alır. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | Resmin yüksekliğini nokta cinsinden alır. 1 nokta 1/72 inçtir. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | Yatay çözünürlüğü DPI olarak alır. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | Dikey çözünürlüğü DPI olarak alır. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | Görüntünün genişliğini piksel cinsinden alır. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | Resmin genişliğini nokta cinsinden alır. 1 nokta 1/72 inçtir. |

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

* property [ImageSize](../imagedata/imagesize/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
