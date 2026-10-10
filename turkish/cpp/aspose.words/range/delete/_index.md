---
title: "Aspose::Words::Range::Delete metodu"
linktitle: "Sil"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Range::Delete metodu. Aralıktaki tüm karakterleri C++'ta siler."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/range/delete/
---
## Range::Delete method


Aralıktaki tüm karakterleri siler.

```cpp
void Aspose::Words::Range::Delete()
```


## Örnekler



Bir aralıktaki tüm düğümleri nasıl sileceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki ilk bölüme metin ekleyin ve ardından başka bir bölüm ekleyin.
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// Tüm düğümleri kaldırarak ilk bölümü tamamen silin
// kendisinin aralığı içinde, bölümü de dahil olmak üzere.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
