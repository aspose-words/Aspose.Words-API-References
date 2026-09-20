---
title: "Método Aspose::Words::Style::get_List"
linktitle: "get_List"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Style::get_List. Obtiene la lista que define el formato de este estilo de lista en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/style/get_list/
---
## Style::get_List method


Obtiene la lista que define el formato de este estilo de lista.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Style::get_List()
```

## Observaciones


Esta propiedad solo es válida para estilos de lista. Para otros tipos de estilo esta propiedad devuelve **null**.

## Ejemplos



Muestra cómo crear un estilo de lista y usarlo en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Podemos contener un objeto List completo dentro de un estilo.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Cambie la apariencia de todos los niveles de lista en nuestra lista.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Cree otra lista a partir de una lista dentro de un estilo.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Agregue algunos elementos de lista que nuestra lista formateará.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Crear y aplicar otra lista basada en el estilo de lista.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```

## Ver también

* Class [List](../../../aspose.words.lists/list/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
