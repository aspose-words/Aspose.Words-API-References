---
title: "Aspose::Words::BreakType enum"
linktitle: "BreakType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BreakType enum. Bir belge içinde bir kesmenin türünü C++'da belirtir."
type: docs
weight: 82000
url: /tr/cpp/aspose.words/breaktype/
---
## BreakType enum


Bir belge içindeki kesme türünü belirtir.

```cpp
enum class BreakType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| ParagraphBreak | 0 | Paragraflar arasındaki kesme. |
| PageBreak | 1 | Açık sayfa kesmesi. |
| ColumnBreak | 2 | Açık sütun kesmesi. |
| SectionBreakContinuous | 3 | Önceki bölümle aynı sayfada yeni bir bölümün başlangıcını belirtir. |
| SectionBreakNewColumn | 4 | Yeni sütunda yeni bir bölümün başlangıcını belirtir. |
| SectionBreakNewPage | 5 | Yeni bir sayfada yeni bir bölümün başlangıcını belirtir. |
| SectionBreakEvenPage | 6 | Yeni bir çift sayfada yeni bir bölümün başlangıcını belirtir. |
| SectionBreakOddPage | 7 | Tek sayfada yeni bir bölümün başlangıcını belirtir. |
| LineBreak | 8 | Açık satır kesmesi. |


## Örnekler



Başlık stillerini giriş olarak kullanarak bir belgeye İçindekiler Tablosu (TOC) eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgenin ilk sayfası için bir içindekiler tablosu ekleyin.
// Tabloyu, 1 ila 3 seviyelerindeki başlıklarla paragraf alacak şekilde yapılandırın.
// Ayrıca, girdilerini bizi yönlendirecek hiperlinkler olarak ayarlayın
// Microsoft Word'de sol tıklandığında başlığın konumuna.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// İçindekiler tablosunu, başlık stilleriyle paragraflar ekleyerek doldurun.
// 1 ile 3 arasında bir seviyeye sahip her başlık, tabloda bir giriş oluşturur.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// İçindekiler tablosu, güncel bir sonuç göstermek için güncellenmesi gereken bir tür alanıdır.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Oluşturucunun geçerli bölümü için sayfa ayarı özelliklerini değiştirin ve metin ekleyin.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Bir belge oluşturucu kullanarak yeni bir bölüm başlatırsak,
// oluşturucunun geçerli sayfa ayarı özelliklerini devralacaktır.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Sayfa ayarı özelliklerini varsayılan değerlerine geri döndürmek için "ClearFormatting" yöntemini kullanabiliriz.
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
