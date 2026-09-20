---
title: "Método Aspose::Words::PhoneticGuide::get_BaseText"
linktitle: "get_BaseText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PhoneticGuide::get_BaseText. Obtiene el texto base de la guía fonética en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/phoneticguide/get_basetext/
---
## PhoneticGuide::get_BaseText method


Obtiene el texto base de la guía fonética.

```cpp
System::String Aspose::Words::PhoneticGuide::get_BaseText()
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

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
