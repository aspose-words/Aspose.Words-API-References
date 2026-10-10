---
title: "Aspose::Words::PageSetup::get_Gutter metodu"
linktitle: "get_Gutter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_Gutter metodu. C++'ta belge bağlaması için kenara eklenen ekstra boşluk miktarını alır veya ayarlar."
type: docs
weight: 18000
url: /tr/cpp/aspose.words/pagesetup/get_gutter/
---
## PageSetup::get_Gutter method


Belge ciltleme için kenara eklenen ekstra boşluk miktarını alır veya ayarlar.

```cpp
double Aspose::Words::PageSetup::get_Gutter()
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


Bir belgenin kitap katlaması olarak nasıl yapılandırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 16 sayfayı kapsayan metin ekleyin.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Belgeyi kitap katlaması biçiminde yazdırmak için ilk bölümün "PageSetup" özelliğini yapılandırın.
// Bu belgeyi iki taraflı yazdırdığımızda, sayfaları alıp üst üste koyabiliriz
// ve hepsini bir anda ortasından katlayabiliriz. Belgenin içeriği bir kitap katlaması şeklinde hizalanacaktır.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Sayfa sayısını yalnızca 4'ün katları olarak belirtebiliriz.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
