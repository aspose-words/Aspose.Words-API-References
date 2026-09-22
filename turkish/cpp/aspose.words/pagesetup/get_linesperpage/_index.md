---
title: "Aspose::Words::PageSetup::get_LinesPerPage yöntemi"
linktitle: "get_LinesPerPage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_LinesPerPage yöntemi. C++'da belge ızgarasında sayfa başına satır sayısını alır veya ayarlar."
type: docs
weight: 26000
url: /tr/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


Belge ızgarasındaki sayfa başına satır sayısını alır veya ayarlar.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## Açıklamalar


Özelliğin minimum değeri 1'dir. Maksimum değer, sayfa yüksekliği ve Normal stilinin yazı tipi boyutuna bağlıdır. Minimum satır aralığı, yazı tipi boyutunun %136'sıdır. Örneğin, bir inç kenar boşluklu Letter sayfasında sayfa başına maksimum satır sayısı 39'dur.

Varsayılan olarak, özellik bir değere sahiptir; bu değerde satır aralığı, Normal stilinin yazı tipi boyutunun 1,5 katı kadardır.

## Örnekler



Her sayfada bulunabilecek satır sayısı için bir sınır nasıl belirlenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Kaydırmayı etkinleştirin ve ardından bu bölümde sayfa başına satır sayısını ayarlamak için kullanın.
// Yeterince büyük bir yazı tipi boyutu, karakterlerin üst üste gelmesini önlemek için bazı satırları bir sonraki sayfaya itecektir.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
