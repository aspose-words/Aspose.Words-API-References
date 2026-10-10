---
title: "Aspose::Words::Lists::ListLevel::GetEffectiveValue Methode"
linktitle: "GetEffectiveValue"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLevel::GetEffectiveValue-Methode. Gibt die Zeichenkettenrepräsentation des ListLevel-Objekts für den angegebenen Index des Listenelements zurück. Parameter geben den NumberStyle und eine optionale Formatzeichenfolge an, die verwendet wird, wenn Custom in C++ angegeben ist."
type: docs
weight: 1000
url: /de/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


Gibt die Zeichenkettenrepräsentation des [ListLevel](../)-Objekts für den angegebenen Index des Listenelements zurück. Parameter geben den [NumberStyle](../../../aspose.words/numberstyle/) und eine optionale Formatzeichenfolge an, die verwendet wird, wenn [Custom](../../../aspose.words/numberstyle/) angegeben ist.

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Der Index des Listenelements (muss im Bereich von 1 bis 32767 liegen). |
| numberStyle | Aspose::Words::NumberStyle | Der [NumberStyle](../../../aspose.words/numberstyle/) des [ListLevel](../)-Objekts. |
| customNumberStyleFormat | const System::String\& | Die optionale Formatzeichenfolge, die verwendet wird, wenn [Custom](../../../aspose.words/numberstyle/) angegeben ist (z. B. \"a, ç, ĝ, ...\"). In anderen Fällen muss dieser Parameter **null** oder leer sein. |

### ReturnValue

Die Zeichenkettenrepräsentation des [ListLevel](../)-Objekts, beschrieben durch den *numberStyle*-Parameter und den *customNumberStyleFormat*-Parameter, im Listenelement an der durch den *index*-Parameter bestimmten Position.

## Beispiele



Zeigt, wie das Format für eine Liste mit dem benutzerdefinierten Zahlenstil abgerufen wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// Wir können den Wert für den angegebenen Index des Listenelements erhalten.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```

## Siehe auch

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
