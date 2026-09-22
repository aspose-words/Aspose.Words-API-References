---
title: "Aspose::Words::Range::UnlinkFields method"
linktitle: "UnlinkFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Range::UnlinkFields metodu. C++'ta bu aralıktaki alanların bağlantısını kaldırır."
type: docs
weight: 14000
url: /tr/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


Bu aralıktaki alanların bağlantısını kaldırır.

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## Açıklamalar


Bu aralıktaki tüm alanları en son sonuçlarıyla değiştirir.

Tüm belgede alanların bağlantısını kaldırmak için [UnlinkFields](./) kullanın.

## Örnekler



Bir aralıktaki tüm alanların bağlantısını nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## Ayrıca Bakınız

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
