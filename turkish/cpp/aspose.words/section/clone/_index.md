---
title: "Aspose::Words::Section::Clone yöntemi"
linktitle: "Clone"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Section::Clone yöntemi. Bu bölümün bir kopyasını C++'ta oluşturur."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/section/clone/
---
## Section::Clone method


Bu bölümün bir kopyasını oluşturur.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Section::Clone()
```


## Örnekler



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

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
