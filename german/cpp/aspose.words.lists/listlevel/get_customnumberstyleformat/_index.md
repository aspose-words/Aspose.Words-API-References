---
title: "Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat Methode"
linktitle: "get_CustomNumberStyleFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat Methode. Ruft das benutzerdefinierte Zahlenformat für diese Listenebene ab oder legt es fest. Zum Beispiel: \"a, ç, ĝ, ...\" in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.lists/listlevel/get_customnumberstyleformat/
---
## ListLevel::get_CustomNumberStyleFormat method


Liest oder setzt das benutzerdefinierte Zahlenstilformat für diese Listenebene. Zum Beispiel: "a, ç, ĝ, ...".

```cpp
System::String Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat()
```


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


Zeigt, wie das benutzerdefinierte Zahlenstilformat festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"001.", paras->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"0001.", paras->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"0002.", paras->idx_get(2)->get_ListLabel()->get_LabelString());

paras->idx_get(1)->get_ListFormat()->get_ListLevel()->set_CustomNumberStyleFormat(u"001, 002, 003, ...");

doc->UpdateListLabels();

ASSERT_EQ(u"001.", paras->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"001.", paras->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"002.", paras->idx_get(2)->get_ListLabel()->get_LabelString());
```

## Siehe auch

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
