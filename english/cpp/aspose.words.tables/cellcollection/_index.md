---
title: CellCollection
second_title: Aspose.Words for C++ API Reference
description: Provides typed access to a collection of Cell nodes.
type: docs
weight: 14
url: /cpp/aspose.words.tables/cellcollection/
---
## CellCollection class


Provides typed access to a collection of [Cell](../cell/) nodes.

```cpp
class CellCollection : public Aspose::Words::NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determines whether a node is in the collection. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [idx_get](./idx_get/)(int32_t) | Retrieves a **Cell** at the given index. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all cells from the collection to a new array of cells. |

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

## See Also

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words](../../)
