---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words for .NET
description: MetafileRenderingOptions UseGdiRasterOperationsEmulation mülk. Tarama işlemleri emülasyonu için GDInın kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Tarama işlemleri emülasyonu için GDI+'nın kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Notlar

Tarama işlemlerini taklit etmek için Windows GDI+ kitaplığı kullanılabilir. Aspose.Word'ün kendi emülasyonuna kıyasla tüm tarama işlemleri için destek sağlar ancak bazı durumlarda performans daha yavaş olabilir.

Bu değer şu şekilde ayarlandığında`doğru`Aspose.Words tarama işlemleri emülasyonu için GDI+'ı kullanır.

Bu değer şu şekilde ayarlandığında`YANLIŞ`Aspose.Words kendi tarama işlemleri emülasyonu uygulamasını kullanır.

Bu seçenek yalnızca meta dosyası vektör grafikleri olarak işlendiğinde kullanılır.

Varsayılan değer:`YANLIŞ`.

## Örnekler

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

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
