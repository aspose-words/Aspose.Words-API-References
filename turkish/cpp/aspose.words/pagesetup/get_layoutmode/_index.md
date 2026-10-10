---
title: "Aspose::Words::PageSetup::get_LayoutMode yöntemi"
linktitle: "get_LayoutMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_LayoutMode metodu. Bu bölümün düzen modunu C++'ta alır veya ayarlar."
type: docs
weight: 21000
url: /tr/cpp/aspose.words/pagesetup/get_layoutmode/
---
## PageSetup::get_LayoutMode method


Bu bölümün yerleşim modunu alır veya ayarlar.

```cpp
Aspose::Words::SectionLayoutMode Aspose::Words::PageSetup::get_LayoutMode()
```


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

* Enum [SectionLayoutMode](../../sectionlayoutmode/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
