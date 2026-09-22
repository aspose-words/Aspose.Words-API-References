---
title: "Aspose::Words::SectionLayoutMode enum"
linktitle: "SectionLayoutMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::SectionLayoutMode enum. Bir bölüm için düzen modunu belirler ve C++'da belge ızgara davranışını tanımlamaya izin verir."
type: docs
weight: 115000
url: /tr/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


Bir bölüm için belge ızgara davranışını tanımlamaya izin veren düzen modunu belirtir.

```cpp
enum class SectionLayoutMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Default | 0 | Belgedeki ilgili bölümün içeriğine hiçbir belge ızgarasının uygulanmayacağını belirtir. |
| Izgara | 1 | İlgili bölümün, sayfa başına belirli bir satır sayısı ve satır başına karakter sayısını korumak amacıyla, her satıra ve karaktere ek satır aralığı ve karakter aralığı ekleyeceğini belirtir. Karakterler, yazarken ızgara çizgilerine otomatik olarak hizalanmayacaktır. |
| LineGrid | 2 | İlgili bölümün, sayfa başına belirtilen satır sayısını korumak için her satıra ek satır aralığı ekleyeceğini belirtir. |
| SnapToChars | 3 | İlgili bölümün, sayfa başına belirli bir satır sayısı ve satır başına karakter sayısını korumak amacıyla, her satıra ve karaktere ek satır aralığı ve karakter aralığı ekleyeceğini belirtir. Karakterler, yazarken otomatik olarak ızgara çizgilerine hizalanacaktır. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
