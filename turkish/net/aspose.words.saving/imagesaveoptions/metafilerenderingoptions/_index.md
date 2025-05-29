---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: .NET için Aspose.Words
description: Geliştirilmiş görüntü kalitesi için işlenmiş çıktınızdaki meta dosyası işlemeyi kontrol etmek üzere ImageSaveOptions MetafileRenderingOptions özelliğini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Meta dosyalarının işlenen çıktıda nasıl işleneceğini belirtmeye izin verir.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Notlar

Ne zamanVector belirtildiğinde, Aspose.Words renders metafile dosyasını önce kendi metafile işleme motorunu kullanarak vektör grafiklere dönüştürür ve ardından vector grafiklerini görüntüye işler.

Ne zamanBitmap belirtildiğinde, Aspose.Words renders meta dosyasını GDI+ meta dosyası oluşturma motorunu kullanarak doğrudan görüntüye ekler.

GDI+ meta dosyası oluşturma motoru daha hızlı çalışır, hemen hemen tüm meta dosyası özelliklerini destekler ancak düşük çözünürlüklerde sayfadaki diğer vektör grafikleriyle (özellikle metin için) karşılaştırıldığında tutarsız sonuçlar üretebilir. Aspose.Words meta dosyası oluşturma motoru düşük çözünürlüklerde even daha tutarlı sonuçlar üretecektir ancak daha yavaş çalışır ve karmaşık meta dosyalarını yanlış bir şekilde oluşturabilir.

Varsayılan değer[`MetafileRenderingMode`](../../metafilerenderingmode/) dırBitmap.

## Örnekler

Windows Meta Dosyası görüntülerini diğer görüntü biçimlerine kaydederken işleme modunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// Belgeyi bir resim olarak kaydettiğimizde, SaveOptions nesnesini görüntüye geçirebiliriz.
// Kaydetme işleminin belgedeki Windows Meta Dosyalarını nasıl işleyeceğini belirleyin.
// "RenderingMode" özelliğini "MetafileRenderingMode.Vector" olarak ayarlarsak,
// veya "MetafileRenderingMode.VectorWithFallback", tüm meta dosyalarını vektör grafikleri olarak oluşturacağız.
// "RenderingMode" özelliğini "MetafileRenderingMode.Bitmap" olarak ayarlarsak tüm meta dosyalarını bitmap olarak oluştururuz.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words, değeri true olarak ayarlandığında raster işlemleri emülasyonu için GDI+ kullanır.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
