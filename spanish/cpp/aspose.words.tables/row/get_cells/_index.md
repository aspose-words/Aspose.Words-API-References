---
title: "Método Aspose::Words::Tables::Row::get_Cells"
linktitle: "get_Cells"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Row::get_Cells. Proporciona acceso tipado a los nodos hijo Cell de la fila en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.tables/row/get_cells/
---
## Row::get_Cells method


Proporciona acceso tipado a los nodos hijo [Cell](../../cell/) de la fila.

```cpp
System::SharedPtr<Aspose::Words::Tables::CellCollection> Aspose::Words::Tables::Row::get_Cells()
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

## Ver también

* Class [CellCollection](../../cellcollection/)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
