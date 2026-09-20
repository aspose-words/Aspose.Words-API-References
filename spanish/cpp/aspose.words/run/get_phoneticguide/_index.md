---
title: "Método Aspose::Words::Run::get_PhoneticGuide"
linktitle: "get_PhoneticGuide"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Run::get_PhoneticGuide. Obtiene un objeto PhoneticGuide en C++."
type: docs
weight: 4500
url: /es/cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


Obtiene un objeto [PhoneticGuide](./).

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
```


## Ejemplos



Muestra cómo obtener las propiedades de la guía fonética.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// Utilice la guía fonética en el texto asiático.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## Ver también

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
