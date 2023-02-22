---
title: Class ImageSize
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.ImageSize sınıf. Görüntü boyutu ve çözünürlüğü hakkında bilgi içerir.
type: docs
weight: 940
url: /tr/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Görüntü boyutu ve çözünürlüğü hakkında bilgi içerir.

```csharp
public class ImageSize
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ImageSize](imagesize/#constructor)(int, int) | Genişliği ve yüksekliği, piksel cinsinden verilen değerlere sıfırlar. Çözünürlüğü 96 dpi. olarak başlatır |
| [ImageSize](imagesize/#constructor_1)(int, int, double, double) | Genişliği, yüksekliği ve çözünürlüğü verilen değerlere göre başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | Resmin yüksekliğini piksel cinsinden alır. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | Nokta olarak görüntünün yüksekliğini alır. 1 nokta 1/72 inçtir. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | DPI cinsinden yatay çözünürlüğü alır. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | Dikey çözünürlüğü DPI olarak alır. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | Resmin genişliğini piksel olarak alır. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | Nokta olarak görüntünün genişliğini alır. 1 nokta 1/72 inçtir. |

### Örnekler

Bir şeklin bir görüntüyle nasıl yeniden boyutlandırılacağını gösterir.

```csharp
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            // "InsertImage" yöntemini kullanarak bir görüntü eklediğimizde, oluşturucu görüntüyü görüntüleyen şekli ölçekler, böylece,
            // Microsoft Word'de %100 yakınlaştırma kullanarak belgeyi görüntülediğimizde şekil, resmi gerçek boyutunda gösteriyor.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // 400x400 resim, 300x300pt resim boyutunda bir ImageData nesnesi oluşturacaktır.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Bir şeklin boyutları, görüntü verilerinin boyutlarıyla eşleşiyorsa,
            // daha sonra şekil, görüntüyü orijinal boyutunda gösteriyor.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // Şeklin toplam boyutunu %50 küçült.
            shape.Width *= 0.5;

             // Ölçekleme faktörleri, şeklin orantılarını korumak için hem genişlik hem de yükseklik için aynı anda geçerlidir.
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // Şekli yeniden boyutlandırdığımızda, görüntü verilerinin boyutu aynı kalır.
            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Resmin boyutuna göre bir ölçekleme uygulamak için resim veri boyutlarına başvurabiliriz.
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Ayrıca bakınız

* property [ImageSize](../imagedata/imagesize/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


