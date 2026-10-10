---
title: "Aspose::Words::Settings::MultiplePagesType enum"
linktitle: "MultiplePagesType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::MultiplePagesType enum. Belgenin C++'da nasıl yazdırıldığını belirtir."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


Belgenin nasıl yazdırılacağını belirtir.

```cpp
enum class MultiplePagesType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Normal | 0 | Normal baskı, birden fazla sayfa belirtilmemiştir. |
| MirrorMargins | 1 | Karşılıklı sayfalarda sol ve sağ kenar boşluklarını değiştirir. |
| TwoPagesPerSheet | 2 | Her sayfada iki sayfa yazdırır. |
| BookFoldPrinting | 3 | Belgenin kitap katlaması olarak yazdırılıp yazdırılmayacağını belirtir. |
| BookFoldPrintingReverse | 4 | Belgenin ters kitap katlaması olarak yazdırılıp yazdırılmayacağını belirtir. |
| Default | n/a | Varsayılan değer [Normal](./). |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
