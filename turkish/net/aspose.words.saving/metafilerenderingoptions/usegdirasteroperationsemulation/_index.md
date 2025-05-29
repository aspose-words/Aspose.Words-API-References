---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: .NET için Aspose.Words
description: GDI ile raster işlemlerini optimize etmek için MetafileRenderingOptions UseGdiRasterOperationsEmulation özelliğini keşfedin. Performansı ve esnekliği bugün artırın!
type: docs
weight: 80
url: /tr/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

GDI+'ın raster işlemleri emülasyonu için kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Notlar

Windows GDI+ kütüphanesi raster işlemlerini taklit etmek için kullanılabilir. Aspose.Words'ün kendi emülasyonuna kıyasla tüm raster operation için destek sağlar ancak bazı durumlarda performans daha yavaş olabilir.

Bu değer olarak ayarlandığında`doğru`, Aspose.Words, raster işlemlerinin emülasyonu için GDI+ kullanır.

Bu değer olarak ayarlandığında`YANLIŞ`Aspose.Words, raster işlemleri emülasyonunun kendi uygulamasını kullanır.

Bu seçenek yalnızca meta dosyası vektör grafik olarak işlendiğinde kullanılır.

Varsayılan değer:`YANLIŞ`.

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

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
