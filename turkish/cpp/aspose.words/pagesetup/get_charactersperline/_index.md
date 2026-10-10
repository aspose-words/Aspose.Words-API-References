---
title: "Aspose::Words::PageSetup::get_CharactersPerLine metodu"
linktitle: "get_CharactersPerLine"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_CharactersPerLine metodu. C++'ta belge ızgarasındaki satır başına karakter sayısını alır veya ayarlar."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


Belge ızgarasındaki satır başına karakter sayısını alır veya ayarlar.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## Açıklamalar


Özelliğin minimum değeri 1'dir. Maksimum değer, sayfa genişliği ve Normal stilinin yazı tipi boyutuna bağlıdır. Minimum karakter aralığı, yazı tipi boyutunun yüzde 90'ıdır. Örneğin, bir inç kenar boşluklu Letter sayfasında satır başına maksimum karakter sayısı 43'tür.

Varsayılan olarak, özelliğin değeri, karakter aralığının Normal stilinin yazı tipi boyutuna eşit olduğu bir değerdir.

## Örnekler



Her satırın sahip olabileceği karakter sayısını belirtmenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Kaydırmayı etkinleştirin ve ardından bu bölümde satır başına karakter sayısını ayarlamak için kullanın.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// Karakter sayısı ayrıca yazı tipinin boyutuna bağlıdır.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
