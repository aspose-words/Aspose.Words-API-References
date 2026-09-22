---
title: "Aspose::Words::PageSetup::get_RtlGutter yöntemi"
linktitle: "get_RtlGutter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_RtlGutter yöntemi. C++'ta Microsoft Word'ün bölümü sağdan sola ya da soldan sağa dillerine göre oluk (gutter) kullanıp kullanmayacağını alır veya ayarlar."
type: docs
weight: 40000
url: /tr/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


Microsoft Word'ün bölümü sağdan sola ya da soldan sağa dillerine göre oluk (gutter) kullanıp kullanmayacağını alır veya ayarlar.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
```


## Örnekler



Köşe kenar boşluklarını nasıl ayarlayacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Birden fazla sayfaya yayılan metin ekleyin.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Bir gutter, sayfanın sol ya da sağ kenar boşluğuna beyaz boşluklar ekler,
// bu, bir kitaptaki sayfaların ortada katlanmasının sayfa düzenine müdahalesini telafi eder.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Sayfalarımızın kenar boşlukları içinde metin için ne kadar alanı olduğunu belirleyin ve ardından bir kenar boşluğunu doldurmak için bir miktar ekleyin.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// "RtlGutter" özelliğini "true" olarak ayarlayın, böylece gutter sağdan sola metin için daha uygun bir konuma yerleştirilir.
pageSetup->set_RtlGutter(true);

// "MultiplePages" özelliğini "MultiplePagesType.MirrorMargins" olarak ayarlayın, değiştirmek için
// her sayfanın sol/sağ kenar boşluğu konumunu.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
