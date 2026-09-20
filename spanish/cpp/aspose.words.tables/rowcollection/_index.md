---
title: "Aspose::Words::Tables::RowCollection class"
linktitle: "RowCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::RowCollection class. Proporciona acceso tipado a una colección de nodos Row. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.tables/rowcollection/
---
## RowCollection class


Proporciona acceso tipado a una colección de [Row](../row/) nodos. Para obtener más información, visite el artículo de documentación [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class RowCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Recupera un [Row](../row/) en el índice dado. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](./toarray/)() | Copia todas las filas de la colección a una nueva matriz de filas. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo iterar a través de todas las tablas del documento e imprimir el contenido de cada celda.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Podemos usar el método "ToArray" en una colección de filas para clonarla en una matriz.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Podemos usar el método "ToArray" en una colección de celdas para clonarla en una matriz.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## Ver también

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
