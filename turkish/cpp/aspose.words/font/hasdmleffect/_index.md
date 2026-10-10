---
title: "Aspose::Words::Font::HasDmlEffect yöntemi"
linktitle: "HasDmlEffect"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::HasDmlEffect yöntemi. Belirli bir DrawingML metin etkisinin C++'ta uygulanıp uygulanmadığını kontrol eder."
type: docs
weight: 58000
url: /tr/cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


Belirli bir DrawingML metin efektinin uygulanıp uygulanmadığını kontrol eder.

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | DrawingML metin etkisi türü. |

### ReturnValue

**true** if particular DrawingML text effect is applied.

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

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
