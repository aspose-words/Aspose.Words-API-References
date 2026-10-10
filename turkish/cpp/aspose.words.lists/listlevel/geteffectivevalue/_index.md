---
title: "Aspose::Words::Lists::ListLevel::GetEffectiveValue metodu"
linktitle: "GetEffectiveValue"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListLevel::GetEffectiveValue metodu. Belirtilen liste öğesi indeksinin ListLevel nesnesinin dize temsiliini raporlar. Parametreler, Custom belirtildiğinde kullanılan NumberStyle ve isteğe bağlı bir biçim dizesini tanımlar. C++'ta."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


Belirtilen liste öğesinin dizini için [ListLevel](../) nesnesinin dize temsilini rapor eder. Parametreler, [NumberStyle](../../../aspose.words/numberstyle/) ve [Custom](../../../aspose.words/numberstyle/) belirtildiğinde kullanılan isteğe bağlı bir biçim dizesini tanımlar.

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Liste öğesinin dizini (1 ile 32767 arasında olmalıdır). |
| numberStyle | Aspose::Words::NumberStyle | [ListLevel](../) nesnesinin [NumberStyle](../../../aspose.words/numberstyle/) değeri. |
| customNumberStyleFormat | const System::String\& | [Custom](../../../aspose.words/numberstyle/) belirtildiğinde kullanılan isteğe bağlı biçim dizesi (ör. "a, ç, ĝ, ..."). Diğer durumlarda bu parametre **null** veya boş olmalıdır. |

### ReturnValue

*index* parametresiyle belirlenen konumdaki liste öğesindeki [ListLevel](../) nesnesinin, *numberStyle* ve *customNumberStyleFormat* parametreleriyle tanımlanan dize temsili.

## Örnekler



Özel sayı stiliyle bir listenin biçimini nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// Belirtilen liste öğesi indeksinin değerini alabiliriz.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```

## Ayrıca Bakınız

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
