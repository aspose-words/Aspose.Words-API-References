---
title: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions metodu"
linktitle: "get_MetafileRenderingOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions metodu. C++'ta renderlenen çıktıda metafile'ların nasıl işlendiğini belirtmenizi sağlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Renderlenen çıktıda metafillerin nasıl işlendiğini belirtmeye olanak tanır.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Açıklamalar


[Vector](../../metafilerenderingmode/) belirtildiğinde, Aspose.Words önce kendi metafile renderleme motorunu kullanarak metafile'ı vektör grafiklerine dönüştürür ve ardından vektör grafiklerini görüntüye renderler.

[Bitmap](../../metafilerenderingmode/) belirtildiğinde, Aspose.Words GDI+ metafile renderleme motorunu kullanarak metafile'ı doğrudan görüntüye renderler.

GDI+ metafile renderleme motoru daha hızlı çalışır, neredeyse tüm metafile özelliklerini destekler ancak düşük çözünürlüklerde sayfadaki diğer vektör grafiklerle (özellikle metinle) karşılaştırıldığında tutarsız sonuçlar üretebilir. Aspose.Words metafile renderleme motoru düşük çözünürlüklerde bile daha tutarlı sonuçlar verir ancak daha yavaş çalışır ve karmaşık metafile'ları hatalı renderleyebilir.

Varsayılan değer, [MetafileRenderingMode](../../metafilerenderingmode/) için [Bitmap](../../metafilerenderingmode/) olarak ayarlanmıştır.

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

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
