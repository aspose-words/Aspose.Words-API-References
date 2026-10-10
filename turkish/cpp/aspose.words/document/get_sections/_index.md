---
title: "Aspose::Words::Document::get_Sections metodu"
linktitle: "get_Sections"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_Sections metodu. Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür (C++)."
type: docs
weight: 48000
url: /tr/cpp/aspose.words/document/get_sections/
---
## Document::get_Sections method


Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür.

```cpp
System::SharedPtr<Aspose::Words::SectionCollection> Aspose::Words::Document::get_Sections()
```


## Örnekler



Yeni bir bölümün önceki bölüme nasıl ayrıldığını belirtmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"This text is in section 1.");

// Bölüm sonu türleri, yeni bir bölümün önceki bölümden nasıl ayrıldığını belirler.
// Aşağıda beş bölüm sonu türü bulunmaktadır.
// 1 -  Sonraki bölümü yeni bir sayfada başlatır:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"This text is in section 2.");

ASSERT_EQ(Aspose::Words::SectionStart::NewPage, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());

// 2 -  Sonraki bölümü mevcut sayfada başlatır:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"This text is in section 3.");

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, doc->get_Sections()->idx_get(2)->get_PageSetup()->get_SectionStart());

// 3 -  Sonraki bölümü yeni bir çift sayfada başlatır:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Writeln(u"This text is in section 4.");

ASSERT_EQ(Aspose::Words::SectionStart::EvenPage, doc->get_Sections()->idx_get(3)->get_PageSetup()->get_SectionStart());

// 4 -  Sonraki bölümü yeni bir tek sayfada başlatır:
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakOddPage);
builder->Writeln(u"This text is in section 5.");

ASSERT_EQ(Aspose::Words::SectionStart::OddPage, doc->get_Sections()->idx_get(4)->get_PageSetup()->get_SectionStart());

// 5 -  Sonraki bölümü yeni bir sütunda başlatır:
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->SetCount(2);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewColumn);
builder->Writeln(u"This text is in section 6.");

ASSERT_EQ(Aspose::Words::SectionStart::NewColumn, doc->get_Sections()->idx_get(5)->get_PageSetup()->get_SectionStart());

doc->Save(get_ArtifactsDir() + u"PageSetup.SetSectionStart.docx");
```


Bir belgede bölümleri ekleme ve kaldırma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Belgedeki ilk bölümü sil.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Şu anda ilk bölüm olanın bir kopyasını belgenin sonuna ekle.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [SectionCollection](../../sectioncollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
