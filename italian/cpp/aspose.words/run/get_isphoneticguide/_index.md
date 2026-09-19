---
title: "Metodo Aspose::Words::Run::get_IsPhoneticGuide"
linktitle: "get_IsPhoneticGuide"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Run::get_IsPhoneticGuide. Restituisce un valore booleano che indica se il run è una guida fonetica in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words/run/get_isphoneticguide/
---
## Run::get_IsPhoneticGuide method


Restituisce un valore booleano che indica se la sequenza è una guida fonetica.

```cpp
bool Aspose::Words::Run::get_IsPhoneticGuide()
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

* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
