---
title: "Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat método"
linktitle: "get_CustomNumberStyleFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat método. Obtiene o establece el formato de estilo de número personalizado para este nivel de lista. Por ejemplo: \"a, ç, ĝ, ...\" en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.lists/listlevel/get_customnumberstyleformat/
---
## ListLevel::get_CustomNumberStyleFormat method


Obtiene o establece el formato de estilo de número personalizado para este nivel de lista. Por ejemplo: "a, ç, ĝ, ...".

```cpp
System::String Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat()
```


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


Muestra cómo establecer el formato de estilo de número personalizado.
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

## Ver también

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
