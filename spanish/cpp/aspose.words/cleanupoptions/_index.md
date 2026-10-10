---
title: "Clase Aspose::Words::CleanupOptions"
linktitle: "CleanupOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::CleanupOptions. Permite especificar opciones para la limpieza del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/cleanupoptions/
---
## CleanupOptions class


Permite especificar opciones para la limpieza de documentos. Para obtener más información, visite el artículo de documentación [Clean Up a Document](https://docs.aspose.com/words/cpp/clean-up-a-document/).

```cpp
class CleanupOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [CleanupOptions](./cleanupoptions/)() |  |
| [get_DuplicateStyle](./get_duplicatestyle/)() const | Obtiene/establece una bandera que indica si los estilos duplicados deben eliminarse del documento. El valor predeterminado es **false**. |
| [get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/)() const | Especifica que los estilos [BuiltIn](../style/get_builtin/) no utilizados deben eliminarse del documento. |
| [get_UnusedLists](./get_unusedlists/)() const | Especifica si las listas y definiciones de listas no utilizadas deben eliminarse del documento. El valor predeterminado es **true**. |
| [get_UnusedStyles](./get_unusedstyles/)() const | Especifica si los estilos no utilizados deben eliminarse del documento. El valor predeterminado es **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DuplicateStyle](./set_duplicatestyle/)(bool) | Método set para [Aspose::Words::CleanupOptions::get_DuplicateStyle](./get_duplicatestyle/). |
| [set_UnusedBuiltinStyles](./set_unusedbuiltinstyles/)(bool) | Método set para [Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/). |
| [set_UnusedLists](./set_unusedlists/)(bool) | Método set para [Aspose::Words::CleanupOptions::get_UnusedLists](./get_unusedlists/). |
| [set_UnusedStyles](./set_unusedstyles/)(bool) | Método set para [Aspose::Words::CleanupOptions::get_UnusedStyles](./get_unusedstyles/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
