---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet yöntemi"
linktitle: "get_SheetsPerBooklet"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet yöntemi. Her kitapçıkta dahil edilecek sayfa sayısını döndürür veya ayarlar C++'ta."
type: docs
weight: 42000
url: /tr/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


Her kitapçıkta yer alacak sayfa sayısını döndürür veya ayarlar.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


## Örnekler



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
