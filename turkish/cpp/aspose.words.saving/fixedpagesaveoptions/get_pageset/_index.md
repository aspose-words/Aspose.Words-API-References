---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet metodu"
linktitle: "get_PageSet"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet metodu. Render edilecek sayfaları alır veya ayarlar. Varsayılan, C++'ta belgede bulunan tüm sayfalardır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Render edilecek sayfaları alır veya ayarlar. Varsayılan, belgede bulunan tüm sayfalardır.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## Örnekler



Tam sayfa indekslerine göre sayfaların nasıl çıkarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgeye beş sayfa ekleyin.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// \"XpsSaveOptions\" nesnesi oluşturun, bunu belgenin \"Save\" metoduna aktarabiliriz.
// bu yöntemin belgeyi .XPS'ye nasıl dönüştürdüğünü değiştirmek için.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// \"PageSet\" özelliğini kullanarak belgenin bir dizi sayfasını çıktı XPS'ye kaydetmek için seçin.
// Bu durumda, sıfır tabanlı indeks kullanarak yalnızca üç sayfa seçeceğiz: sayfa 1, sayfa 2 ve sayfa 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Ayrıca Bakınız

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
