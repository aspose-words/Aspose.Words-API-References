---
title: "Método Aspose::Words::Run::get_IsPhoneticGuide"
linktitle: "get_IsPhoneticGuide"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Run::get_IsPhoneticGuide. Obtiene un valor booleano que indica si el run es una guía fonética en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words/run/get_isphoneticguide/
---
## Run::get_IsPhoneticGuide method


Obtiene un valor booleano que indica si la ejecución es una guía fonética.

```cpp
bool Aspose::Words::Run::get_IsPhoneticGuide()
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

* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
