---
title: ImageSaveOptions.MetafileRenderingOptions
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. Oluşturulan çıktıda meta dosyalarının nasıl ele alınacağını belirlemeye izin verir.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Oluşturulan çıktıda meta dosyalarının nasıl ele alınacağını belirlemeye izin verir.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

### Notlar

Ne zamanVector belirtildiğinde, Aspose.Words önce kendi meta dosyası oluşturma motorunu kullanarak x000d_ meta dosyasını vektör grafiklerine dönüştürür ve ardından vektör grafiklerini görüntüye işler.

Ne zamanBitmap belirtildiğinde Aspose.Words, GDI+ meta dosyası oluşturma motorunu kullanarak meta dosyasını doğrudan görüntüye işler.

GDI+ meta dosyası oluşturma motoru daha hızlı çalışır, neredeyse tüm meta dosyası özelliklerini destekler ancak düşük çözünürlüklerde, sayfadaki diğer vektör grafikleriyle (özellikle metin için) karşılaştırıldığında tutarsız sonuçlar üretebilir. Aspose.Words meta dosyası oluşturma motoru, düşük çözünürlüklerde even daha tutarlı sonuçlar üretecektir ancak daha yavaş çalışır ve karmaşık meta dosyaları hatalı şekilde görüntüleyebilir.

için varsayılan değer[`MetafileRenderingMode`](../../metafilerenderingmode/) dır-dirBitmap.

### Örnekler

Windows Meta Dosyası görüntüleri içeren belgeleri diğer görüntü formatlarına kaydederken işleme modunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// Belgeyi resim olarak kaydettiğimizde, bir SaveOptions nesnesini iletebiliriz
// kaydetme işleminin belgedeki Windows Meta Dosyalarını nasıl işleyeceğini belirleyin.
// "RenderingMode" özelliğini "MetafileRenderingMode.Vector" olarak ayarlarsak,
// veya "MetafileRenderingMode.VectorWithFallback" ile tüm meta dosyaları vektör grafikleri olarak oluşturacağız.
// "RenderingMode" özelliğini "MetafileRenderingMode.Bitmap" olarak ayarlarsak tüm meta dosyaları bitmap olarak render edeceğiz.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words, değer true olarak ayarlandığında tarama işlemleri emülasyonu için GDI+'yı kullanır.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


