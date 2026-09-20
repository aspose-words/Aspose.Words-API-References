---
title: "Aspose::Words::Lists::ListFormat::get_List método"
linktitle: "get_List"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListFormat::get_List método. Obtiene o establece la lista de la que este párrafo es miembro en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.lists/listformat/get_list/
---
## ListFormat::get_List method


Obtiene o establece la lista a la que pertenece este párrafo.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListFormat::get_List()
```

## Observaciones


La lista que se asigna a esta propiedad debe pertenecer al documento actual.

La lista que se asigna a esta propiedad no debe ser una definición de estilo de lista.

Establecer esta propiedad a **null** elimina viñetas y numeración del párrafo y establece el número de nivel de lista a cero. Establecer esta propiedad a **null** es equivalente a llamar a [RemoveNumbers](../removenumbers/).

## Ejemplos



Muestra cómo trabajar con niveles de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// A continuación se presentan dos tipos de listas que podemos crear usando un document builder.
// 1 -  Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para iniciar una sublista autocontenida en el elemento de lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" usa números para crear niveles de lista para el primer nivel de lista.
// Los niveles de lista más profundos usan letras y números romanos en minúscula.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Una lista con viñetas:
// Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista usarán símbolos diferentes, como "■" y "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Podemos desactivar el formato de lista para que no formatee los párrafos subsecuentes como listas desactivando la bandera "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


Muestra cómo anidar una lista dentro de otra lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Crea una lista de esquema para los encabezados.
System::SharedPtr<Aspose::Words::Lists::List> outlineList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::OutlineNumbers);
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 1");

// Crea una lista numerada.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(numberedList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Numbered list item 1.");

// Cada párrafo que forma parte de una lista tendrá esta bandera.
ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsListItem());
ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsListItem());

// Crea una lista con viñetas.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
builder->get_ListFormat()->set_List(bulletedList);
builder->get_ParagraphFormat()->set_LeftIndent(72);
builder->Writeln(u"Bulleted list item 1.");
builder->Writeln(u"Bulleted list item 2.");
builder->get_ParagraphFormat()->ClearFormatting();

// Vuelve a la lista numerada.
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Numbered list item 2.");
builder->Writeln(u"Numbered list item 3.");

// Vuelve a la lista de esquema.
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 2");

builder->get_ParagraphFormat()->ClearFormatting();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.NestedLists.docx");
```

## Ver también

* Class [List](../../list/)
* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
