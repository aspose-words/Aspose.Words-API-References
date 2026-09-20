---
title: "Aspose::Words::Tables::Table::get_Rows método"
linktitle: "get_Rows"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::get_Rows método. Proporciona acceso tipado a las filas de la tabla en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words.tables/table/get_rows/
---
## Table::get_Rows method


Proporciona acceso tipado a las filas de la tabla.

```cpp
System::SharedPtr<Aspose::Words::Tables::RowCollection> Aspose::Words::Tables::Table::get_Rows()
```


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


Muestra cómo combinar las filas de dos tablas en una sola.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// A continuación se presentan dos formas de obtener una tabla de un documento.
// 1 -  Desde la colección "Tables" de un nodo Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Usando el método "GetChild":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Agregar todas las filas de la tabla actual a la siguiente.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Eliminar el contenedor de tabla vacío.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Ver también

* Class [RowCollection](../../rowcollection/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
