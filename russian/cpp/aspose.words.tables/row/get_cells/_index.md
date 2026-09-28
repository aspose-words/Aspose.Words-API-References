---
title: "Метод Aspose::Words::Tables::Row::get_Cells"
linktitle: "get_Cells"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Row::get_Cells. Предоставляет типизированный доступ к дочерним узлам Cell строки в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.tables/row/get_cells/
---
## Row::get_Cells method


Предоставляет типизированный доступ к дочерним узлам [Cell](../../cell/) строки.

```cpp
System::SharedPtr<Aspose::Words::Tables::CellCollection> Aspose::Words::Tables::Row::get_Cells()
```


## Примеры



Показывает, как пройтись по всем таблицам в документе и вывести содержимое каждой ячейки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Мы можем использовать метод "ToArray" для коллекции строк, чтобы клонировать её в массив.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Мы можем использовать метод "ToArray" для коллекции ячеек, чтобы клонировать её в массив.
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

## См. также

* Class [CellCollection](../../cellcollection/)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
