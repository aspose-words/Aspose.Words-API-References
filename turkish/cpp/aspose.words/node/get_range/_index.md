---
title: "Aspose::Words::Node::get_Range yöntemi"
linktitle: "get_Range"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::get_Range yöntemi. C++'ta bu düğümde bulunan belgenin bir bölümünü temsil eden bir Range nesnesi döndürür."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/node/get_range/
---
## Node::get_Range method


Bu düğümde bulunan belgenin bir bölümünü temsil eden bir [Range](../../range/) nesnesi döndürür.

```cpp
System::SharedPtr<Aspose::Words::Range> Aspose::Words::Node::get_Range()
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

* Class [Range](../../range/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
