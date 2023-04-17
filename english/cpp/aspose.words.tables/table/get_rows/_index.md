---
title: Aspose::Words::Tables::Table::get_Rows method
linktitle: get_Rows
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_Rows method. Provides typed access to the rows of the table in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words.tables/table/get_rows/
---
## Table::get_Rows method


Provides typed access to the rows of the table.

```cpp
System::SharedPtr<Aspose::Words::Tables::RowCollection> Aspose::Words::Tables::Table::get_Rows()
```


## Examples



Shows how to iterate through all tables in the document and print the contents of each cell. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");
SharedPtr<TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int i = 0; i < tables->get_Count(); i++)
{
    std::cout << "Start of Table " << i << std::endl;

    SharedPtr<RowCollection> rows = tables->idx_get(i)->get_Rows();

    // We can use the "ToArray" method on a row collection to clone it into an array.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int j = 0; j < rows->get_Count(); j++)
    {
        std::cout << "\tStart of Row " << j << std::endl;

        SharedPtr<CellCollection> cells = rows->idx_get(j)->get_Cells();

        // We can use the "ToArray" method on a cell collection to clone it into an array.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int k = 0; k < cells->get_Count(); k++)
        {
            String cellText = cells->idx_get(k)->ToString(SaveFormat::Text).Trim();
            std::cout << "\t\tContents of Cell:" << k << " = \"" << cellText << "\"" << std::endl;
        }

        std::cout << "\tEnd of Row " << j << std::endl;
    }

    std::cout << "End of Table " << i << "\n" << std::endl;
}
```


Shows how to combine the rows from two tables into one. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
SharedPtr<Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Using the "GetChild" method:
auto secondTable = System::DynamicCast<Table>(doc->GetChild(NodeType::Table, 1, true));

// Append all rows from the current table to the next.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Remove the empty table container.
secondTable->Remove();

doc->Save(ArtifactsDir + u"Table.CombineTables.docx");
```

## See Also

* Class [RowCollection](../../rowcollection/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
