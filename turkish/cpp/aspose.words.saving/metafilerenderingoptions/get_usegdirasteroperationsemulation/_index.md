---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation yöntemi"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation yöntemi. C++'ta raster işlemlerinin taklit edilmesi için GDI+ kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


Raster işlemlerinin taklit edilmesi için GDI+ kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## Açıklamalar


Windows GDI+ kütüphanesi raster işlemlerini taklit etmek için kullanılabilir. Aspose.Words'ün kendi taklitine kıyasla tüm raster işlemlerini destekler, ancak bazı durumlarda performans daha yavaş olabilir.

Bu değer **true** olarak ayarlandığında, Aspose.Words raster işlemleri taklit etmek için GDI+ kullanır.

Bu değer **false** olarak ayarlandığında, Aspose.Words raster işlemleri taklit etmek için kendi uygulamasını kullanır.

Bu seçenek yalnızca metafile vektör grafik olarak render edildiğinde kullanılır.

Varsayılan değer **false**'tur.

## Örnekler



Windows Metafile görüntüleri içeren belgeleri diğer görüntü formatlarına kaydederken render modunun nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// Belgeyi görüntü olarak kaydettiğimizde, bir SaveOptions nesnesi geçirebiliriz
// Kaydetme işleminin belgede bulunan Windows Metafile'ları nasıl işleyeceğini belirler.
// Eğer "RenderingMode" özelliğini "MetafileRenderingMode.Vector" olarak ayarlarsak,
// veya "MetafileRenderingMode.VectorWithFallback", tüm metafile'ları vektör grafik olarak render edeceğiz.
// Eğer "RenderingMode" özelliğini "MetafileRenderingMode.Bitmap" olarak ayarlarsak, tüm metafile'ları bitmap olarak render edeceğiz.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words, değer true olarak ayarlandığında raster işlemlerinin taklidi için GDI+ kullanır.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## Ayrıca Bakınız

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
