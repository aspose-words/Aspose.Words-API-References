---
title: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution metodu"
linktitle: "get_MaxImageResolution"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution metodu. Dışa aktarılan raster görsellerin çözünürlüğünü sınırlayan, inç başına piksel (ppi) cinsinden bir değeri alır veya ayarlar. Varsayılan değer C++'ta sıfırdır."
type: docs
weight: 4500
url: /tr/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


Dışa aktarılan raster görüntülerin çözünürlüğünü sınırlayan inç başına piksel değerini alır veya ayarlar. Varsayılan değer sıfırdır.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## Açıklamalar


Bu özelliğin değeri sıfırdan farklıysa, dışa aktarılan raster görsellerin çözünürlüğünü sınırlar. Yani, yüksek çözünürlüklü görseller limitin altına yeniden örneklenir ve düşük çözünürlüklü görseller olduğu gibi dışa aktarılır.

Bu özelliğin değeri sıfır ise, tüm raster görseller yeniden örnekleme yapılmadan dışa aktarılır.

## Örnekler



Görsel çözünürlüğü sınırlamayı nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Ayrıca Bakınız

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
