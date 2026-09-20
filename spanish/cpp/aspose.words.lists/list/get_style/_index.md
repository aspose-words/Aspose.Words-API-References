---
title: "Aspose::Words::Lists::List::get_Style método"
linktitle: "get_Style"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::List::get_Style método. Obtiene el estilo de lista que esta lista referencia o define en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.lists/list/get_style/
---
## List::get_Style method


Obtiene el estilo de lista que esta lista referencia o define.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Lists::List::get_Style()
```

## Observaciones


Si esta lista no está asociada a un estilo de lista, la propiedad devolverá **null**.

Una lista podría ser una referencia a un estilo de lista, en este caso [IsListStyleReference](../get_isliststylereference/) será **true**.

Una lista podría ser una definición de un estilo de lista, en este caso [IsListStyleDefinition](../get_isliststyledefinition/) será **true**. Una lista de este tipo no puede aplicarse directamente a los párrafos del documento.

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

* Class [Style](../../../aspose.words/style/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
