---
title: "Aspose::Words::NodeCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeCollection::RemoveAt yöntemi. C++'da belirtilen indeksteki düğümü koleksiyondan ve belgelerden kaldırır."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


Belirtilen indeksteki düğümü koleksiyondan ve belgeden kaldırır.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Düğümün sıfır tabanlı indeksi. Negatif indekslere izin verilir ve listenin sonundan erişimi gösterir. Örneğin -1 son düğüm, -2 sondan bir önceki ve böyle devam eder. |

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

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
