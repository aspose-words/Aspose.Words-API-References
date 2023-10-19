---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ImageSize sınıf. Görüntü boyutu ve çözünürlüğü hakkında bilgi içerir C#'da.
type: docs
weight: 1070
url: /tr/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Görüntü boyutu ve çözünürlüğü hakkında bilgi içerir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Görsellerle Çalışmak](https://docs.aspose.com/words/net/working-with-images/) dokümantasyon makalesi.

```csharp
public class ImageSize
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ImageSize](imagesize/#constructor)(*int, int*) | Genişlik ve yüksekliği piksel cinsinden verilen değerlere göre başlatır. Çözünürlüğü 96 dpi olarak başlatır. |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | Genişliği, yüksekliği ve çözünürlüğü verilen değerlere göre başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | Görüntünün yüksekliğini piksel cinsinden alır. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | Görüntünün yüksekliğini nokta olarak alır. 1 punto 1/72 inçtir. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | Yatay çözünürlüğü DPI cinsinden alır. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | Dikey çözünürlüğü DPI cinsinden alır. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | Görüntünün genişliğini piksel cinsinden alır. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | Görüntünün genişliğini nokta cinsinden alır. 1 punto 1/72 inçtir. |

## Örnekler

Bir şeklin resimle nasıl yeniden boyutlandırılacağını gösterir.

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

            // "InsertImage" yöntemini kullanarak bir görüntü eklediğimizde oluşturucu, görüntüyü görüntüleyen şekli ölçeklendirir;
            // Microsoft Word'de %100 yakınlaştırma kullanarak belgeyi görüntülediğimizde şekil, görüntüyü gerçek boyutunda görüntüler.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // 400x400 boyutunda bir görüntü, 300x300pt boyutunda bir ImageData nesnesi oluşturacaktır.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Bir şeklin boyutları görüntü verilerinin boyutlarıyla eşleşiyorsa,
            // daha sonra şekil, görüntüyü orijinal boyutunda gösteriyor.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // Şeklin genel boyutunu %50 azaltın.
            shape.Width *= 0.5;

             // Ölçekleme faktörleri, şeklin orantılarını korumak için hem genişliğe hem de yüksekliğe aynı anda uygulanır.
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // Şekli yeniden boyutlandırdığımızda resim verisinin boyutu aynı kalıyor.
            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Görüntünün boyutuna göre bir ölçeklendirme uygulamak için görüntü veri boyutlarına başvurabiliriz.
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Ayrıca bakınız

* property [ImageSize](../imagedata/imagesize/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
