---
title: "Aspose::Words::Lists::ListLevel::GetEffectiveValue método"
linktitle: "GetEffectiveValue"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListLevel::GetEffectiveValue método. Informa la representación en cadena del objeto ListLevel para el índice especificado del elemento de la lista. Los parámetros especifican el NumberStyle y una cadena de formato opcional utilizada cuando se especifica Custom en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


Reporta la representación en cadena del objeto [ListLevel](../) para el índice especificado del elemento de lista. Los parámetros especifican el [NumberStyle](../../../aspose.words/numberstyle/) y una cadena de formato opcional utilizada cuando se especifica [Custom](../../../aspose.words/numberstyle/).

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice del elemento de lista (debe estar en el rango de 1 a 32767). |
| numberStyle | Aspose::Words::NumberStyle | El [NumberStyle](../../../aspose.words/numberstyle/) del objeto [ListLevel](../). |
| customNumberStyleFormat | const System::String\& | La cadena de formato opcional utilizada cuando se especifica [Custom](../../../aspose.words/numberstyle/) (p. ej., "a, ç, ĝ, ..."). En otros casos, este parámetro debe ser **null** o estar vacío. |

### ReturnValue

La representación en cadena del objeto [ListLevel](../), descrita por el parámetro *numberStyle* y el parámetro *customNumberStyleFormat*, en el elemento de lista en la posición determinada por el parámetro *index*.

## Ejemplos



Muestra cómo obtener el formato para una lista con el estilo de número personalizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// Podemos obtener el valor para el índice especificado del elemento de la lista.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```

## Ver también

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
