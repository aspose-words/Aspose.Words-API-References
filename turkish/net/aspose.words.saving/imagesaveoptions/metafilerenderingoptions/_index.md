---
title: ImageSaveOptions.MetafileRenderingOptions
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. İşlenen çıktıda meta dosyaların nasıl ele alınacağını belirlemeye izin verir.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

İşlenen çıktıda meta dosyaların nasıl ele alınacağını belirlemeye izin verir.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

### Notlar

Ne zamanVector belirtildiğinde, Aspose.Words önce kendi metafile oluşturma motorunu kullanarak vektör grafiklerine metafile işler ve ardından vector grafiklerini görüntüye işler.

Ne zamanBitmap Aspose.Words, GDI+ meta dosyası oluşturma motorunu kullanarak doğrudan görüntüye meta dosyasını oluşturur.

GDI+ meta dosyası oluşturma motoru daha hızlı çalışır, neredeyse tüm meta dosyası özelliklerini destekler, ancak düşük çözünürlüklerde, sayfadaki diğer vektör grafikleriyle (özellikle metin için) karşılaştırıldığında tutarsız sonuçlar verebilir. Aspose.Words meta dosyası oluşturma motoru, düşük çözünürlüklerde bile daha tutarlı sonuç verir ancak daha yavaş çalışır ve karmaşık meta dosyaları hatalı bir şekilde oluşturabilir.

için varsayılan değer[`MetafileRenderingMode`](../../metafilerenderingmode/) dır-dirBitmap.

### Örnekler

Windows Meta Dosyası görüntüleri içeren belgeleri diğer görüntü biçimlerine kaydederken işleme modunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// Belgeyi bir resim olarak kaydettiğimizde, bir SaveOptions nesnesini şuraya aktarabiliriz:
// kaydetme işleminin belgedeki Windows Meta Dosyalarını nasıl işleyeceğini belirleyin.
// "RenderingMode" özelliğini "MetafileRenderingMode.Vector" olarak ayarlarsak,
// veya "MetafileRenderingMode.VectorWithFallback", tüm meta dosyaları vektör grafikleri olarak oluşturacağız.
// "RenderingMode" özelliğini "MetafileRenderingMode.Bitmap" olarak ayarlarsak tüm meta dosyaları bitmap olarak işleyeceğiz.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


