---
title: "Aspose::Words::Tables::TableCollection class"
linktitle: "TableCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::TableCollection class. Proporciona acceso tipado a una colección de nodos Table. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.tables/tablecollection/
---
## TableCollection class


Proporciona acceso tipado a una colección de [Table](../table/) nodos. Para obtener más información, visite el artículo de documentación [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableCollection : public Aspose::Words::NodeCollection
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina si un nodo está en la colección. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Obtiene el número de nodos en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera un [Table](../table/) en el índice dado. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](./toarray/)() | Copia todas las tablas de la colección a una nueva matriz de tablas. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo eliminar la primera y la última fila de todas las tablas en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(5, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(4, tables->idx_get(1)->get_Rows()->get_Count());

for (auto&& table : System::IterateOver(tables->LINQ_OfType<System::SharedPtr<Aspose::Words::Tables::Table> >()))
{
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression = table->get_FirstRow();
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression2 = table->get_LastRow();
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }
}

ASSERT_EQ(3, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(2, tables->idx_get(1)->get_Rows()->get_Count());
```

## Ver también

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
