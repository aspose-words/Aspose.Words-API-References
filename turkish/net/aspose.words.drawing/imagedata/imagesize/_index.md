---
title: ImageData.ImageSize
second_title: Aspose.Words for .NET API Referansı
description: ImageData mülk. Görüntü boyutu ve çözünürlüğü hakkında bilgi alır.
type: docs
weight: 130
url: /tr/net/aspose.words.drawing/imagedata/imagesize/
---
## ImageData.ImageSize property

Görüntü boyutu ve çözünürlüğü hakkında bilgi alır.

```csharp
public ImageSize ImageSize { get; }
```

### Notlar

Görüntü yalnızca bağlantılıysa ve belgede saklanmıyorsa sıfır boyut döndürür.

### Örnekler

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

* class [ImageSize](../../imagesize/)
* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../imagedata/)
* toplantı [Aspose.Words](../../../)


