---
title: "Aspose::Words::Lists::ListLevel::GetEffectiveValue metod"
linktitle: "GetEffectiveValue"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListLevel::GetEffectiveValue metod. Rapporterar strängrepresentationen av ListLevel‑objektet för det angivna indexet för listobjektet. Parametrar anger NumberStyle och en valfri formatsträng som används när Custom anges i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


Rapporterar strängrepresentationen av [ListLevel](../)‑objektet för det angivna indexet för listobjektet. Parametrar anger [NumberStyle](../../../aspose.words/numberstyle/) och en valfri formatsträng som används när [Custom](../../../aspose.words/numberstyle/) anges.

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Indexet för listobjektet (måste vara i intervallet 1 till 32767). |
| numberStyle | Aspose::Words::NumberStyle | [NumberStyle](../../../aspose.words/numberstyle/) för [ListLevel](../)‑objektet. |
| customNumberStyleFormat | const System::String\& | Den valfria formatsträngen som används när [Custom](../../../aspose.words/numberstyle/) anges (t.ex. "a, ç, ĝ, ..."). I andra fall måste denna parameter vara **null** eller tom. |

### ReturnValue

Strängrepresentationen av objektet [ListLevel](../), beskriven av parametern *numberStyle* och parametern *customNumberStyleFormat*, i listobjektet på den position som bestäms av parametern *index*.

## Exempel



Visar hur man hämtar formatet för en lista med anpassad nummerstil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// Vi kan hämta värdet för det angivna indexet för listobjektet.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```

## Se även

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
