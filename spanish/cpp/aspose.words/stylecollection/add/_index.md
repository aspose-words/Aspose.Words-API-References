---
title: "Aspose::Words::StyleCollection::Add método"
linktitle: "Add"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::StyleCollection::Add método. Crea un nuevo estilo definido por el usuario y lo agrega a la colección en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


Crea un nuevo estilo definido por el usuario y lo agrega a la colección.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| type | Aspose::Words::StyleType | Un valor [StyleType](../../styletype/) que especifica el tipo de estilo a crear. |
| name | const System::String\& | Nombre sensible a mayúsculas y minúsculas del estilo a crear. |
## Observaciones


Puede crear un estilo de carácter, de párrafo o de lista.

Al crear un estilo de lista, el estilo se crea con el formato de lista numerada predeterminado (1 \\ a \\ i).

Lanza una excepción si ya existe un estilo con este nombre.

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


Muestra cómo agregar un [Style](../../style/) a la colección de estilos de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Establezca los parámetros predeterminados para los nuevos estilos que luego podamos agregar a esta colección.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Si añadimos un estilo de "StyleType.Paragraph", la colección aplicará los valores de
// su propiedad "DefaultParagraphFormat" a la propiedad "ParagraphFormat" del estilo.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Añade un estilo y luego verifica que tiene la configuración predeterminada.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ver también

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
