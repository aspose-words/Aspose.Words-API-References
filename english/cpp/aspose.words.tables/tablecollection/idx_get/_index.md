---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Retrieves a Table at the given index.
type: docs
weight: 1
url: /cpp/aspose.words.tables/tablecollection/idx_get/
---
## TableCollection.idx_get method


Retrieves a **Table** at the given index.

```cpp
System::SharedPtr<Aspose::Words::Tables::Table> Aspose::Words::Tables::TableCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection. |

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

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
