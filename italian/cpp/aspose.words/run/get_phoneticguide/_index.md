---
title: "Metodo Aspose::Words::Run::get_PhoneticGuide"
linktitle: "get_PhoneticGuide"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Run::get_PhoneticGuide. Ottiene un oggetto PhoneticGuide in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


Ottiene un oggetto [PhoneticGuide](./).

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
```


## Esempi



Mostra come ottenere le proprietà della guida fonetica.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// Utilizza la guida fonetica nel testo asiatico.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## Vedi anche

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
