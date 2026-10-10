---
title: "Aspose::Words::Section::ClearContent yöntemi"
linktitle: "ClearContent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Section::ClearContent yöntemi. Bölümü C++'ta temizler."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


Bölümü temizler.

```cpp
void Aspose::Words::Section::ClearContent()
```

## Açıklamalar


[Body](../get_body/) metni temizlenir, sadece bölüm sonunu temsil eden bir boş paragraf kalır.

Tüm başlık ve altbilgilerin metni temizlenir, ancak [HeaderFooter](../../headerfooter/) nesneleri kendileri kaldırılmaz.

## Örnekler



Bir bölümün içeriğini nasıl temizleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// "ClearContent" yöntemini çalıştırmak, bölümün tüm içeriğini kaldıracaktır
// ancak içeriği tekrar eklemek için boş bir paragraf bırakır.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## Ayrıca Bakınız

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
