---
title: "Aspose::Words::TextDmlEffect enum"
linktitle: "TextDmlEffect"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextDmlEffect enum. C++'de metin koşularında Dml metin efekti."
type: docs
weight: 122000
url: /tr/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


Metin çalıştırmaları için Dml metin efekti.

```cpp
enum class TextDmlEffect
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Glow | 0 | Glow efekti, nesnenin kenarlarının dışına renkli bulanık bir kontur eklenir. |
| Fill | 1 | Fill bindirme efekti. |
| Shadow | 2 | Shadow efekti. |
| Outline | 3 | Outline efekti. |
| Effect3D | 4 | 3B efekti. |
| Reflection | 5 | Reflection efekti. |


## Örnekler



Bir koşunun DrawingML metin efekti gösterip göstermediğini nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
