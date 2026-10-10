---
title: "Aspose::Words::Document::Cleanup método"
linktitle: "Cleanup"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::Cleanup método. Elimina estilos y listas no utilizados del documento en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/document/cleanup/
---
## Document::Cleanup() method


Elimina estilos y listas no utilizados del documento.

```cpp
void Aspose::Words::Document::Cleanup()
```


## Ejemplos



Muestra cómo eliminar estilos personalizados no utilizados de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// Combinado con los estilos incorporados, el documento ahora tiene ocho estilos.
// Un estilo personalizado se considera "usado" mientras esté aplicado a alguna parte del documento,
// lo que significa que los cuatro estilos que añadimos están actualmente sin usar.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Aplique un estilo de carácter personalizado y luego un estilo de lista personalizado. Hacer esto marcará los estilos como "usados".
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Cleanup();

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Eliminar cada nodo al que se aplique un estilo personalizado lo marca como "unused" de nuevo.
// Ejecute el método Cleanup nuevamente para eliminarlos.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup();

ASSERT_EQ(4, doc->get_Styles()->get_Count());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Cleanup(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) method


Elimina estilos y listas no utilizados del documento según las [CleanupOptions](../../cleanupoptions/) proporcionadas.

```cpp
void Aspose::Words::Document::Cleanup(const System::SharedPtr<Aspose::Words::CleanupOptions> &options)
```


## Ejemplos



Muestra cómo eliminar todos los estilos personalizados no utilizados de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// Combinado con los estilos incorporados, el documento ahora tiene ocho estilos.
// Un estilo personalizado se marca como "used" mientras haya cualquier texto dentro del documento
// formateado en ese estilo. Esto significa que los 4 estilos que añadimos están actualmente sin usar.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Aplica un estilo de carácter personalizado y luego un estilo de lista personalizado. Hacer esto los marcará como "used".
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// Ahora, hay un estilo de carácter sin usar y un estilo de lista sin usar.
// El método Cleanup(), cuando se configura con un objeto CleanupOptions, puede dirigirse a los estilos sin usar y eliminarlos.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Eliminar cada nodo al que se aplique un estilo personalizado lo marca como "unused" de nuevo.
// Vuelve a ejecutar el método Cleanup para eliminarlos.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## Ver también

* Class [CleanupOptions](../../cleanupoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
