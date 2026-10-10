---
title: "Método Aspose::Words::CleanupOptions::get_UnusedLists"
linktitle: "get_UnusedLists"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::CleanupOptions::get_UnusedLists. Especifica si las listas y definiciones de listas no utilizadas deben eliminarse del documento. El valor predeterminado es true en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/cleanupoptions/get_unusedlists/
---
## CleanupOptions::get_UnusedLists method


Especifica si las listas y definiciones de listas no utilizadas deben eliminarse del documento. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::CleanupOptions::get_UnusedLists() const
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

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
