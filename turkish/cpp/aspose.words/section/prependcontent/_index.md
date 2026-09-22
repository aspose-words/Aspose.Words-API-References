---
title: "Aspose::Words::Section::PrependContent yöntemi"
linktitle: "PrependContent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Section::PrependContent yöntemi. C++'ta kaynak bölümün içeriğinin bir kopyasını bu bölümün başına ekler."
type: docs
weight: 17000
url: /tr/cpp/aspose.words/section/prependcontent/
---
## Section::PrependContent method


Kaynak bölümün içeriğinin bir kopyasını bu bölümün başına ekler.

```cpp
void Aspose::Words::Section::PrependContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | İçeriği kopyalanacak bölüm. |
## Açıklamalar


Sadece kaynak bölümün [Body](../get_body/) içeriği kopyalanır, sayfa ayarı, üstbilgiler ve altbilgiler kopyalanmaz.

Kaynak bölüm farklı bir belgeye aitse, düğümler otomatik olarak içe aktarılır.

Hedef belgede yeni bir bölüm oluşturulmaz.

## Örnekler



Bir bölümün içeriğini başka bir bölüme eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

System::SharedPtr<Aspose::Words::Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(System::String(u"Section 3") + Aspose::Words::ControlChar::SectionBreak(), section->GetText());

// İlk bölümün içeriğini üçüncü bölümün başına ekleyin.
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// İkinci bölümün içeriğini üçüncü bölümün sonuna ekleyin.
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// \"PrependContent\" ve \"AppendContent\" yöntemleri yeni bir bölüm oluşturmadı.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## Ayrıca Bakınız

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
