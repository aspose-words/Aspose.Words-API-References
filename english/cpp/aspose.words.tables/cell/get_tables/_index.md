---
title: get_Tables
second_title: Aspose.Words for C++ API Reference
description: Gets a collection of tables that are immediate children of the cell.
type: docs
weight: 157
url: /cpp/aspose.words.tables/cell/get_tables/
---
## Cell::get_Tables method


Gets a collection of tables that are immediate children of the cell.

```cpp
System::SharedPtr<Aspose::Words::Tables::TableCollection> Aspose::Words::Tables::Cell::get_Tables()
```


## Examples



Shows how to find out if a tables are nested. 
```cpp
void CalculateDepthOfNestedTables()
{
    auto doc = MakeObject<Document>(MyDir + u"Nested tables.docx");
    SharedPtr<NodeCollection> tables = doc->GetChildNodes(NodeType::Table, true);

    for (int i = 0; i < tables->get_Count(); i++)
    {
        auto table = System::DynamicCast<Table>(tables->idx_get(i));

        // Find out if any cells in the table have other tables as children.
        int count = GetChildTableCount(table);
        std::cout << "Table #" << i << " has " << count << " tables directly within its cells" << std::endl;

        // Find out if the table is nested inside another table, and, if so, at what depth.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
        {
            std::cout << "Table #" << i << " is nested inside another table at depth of " << tableDepth << std::endl;
        }
        else
        {
            std::cout << "Table #" << i << " is a non nested table (is not a child of another table)" << std::endl;
        }
    }
}

static int GetNestedDepthOfTable(SharedPtr<Table> table)
{
    int depth = 0;
    SharedPtr<Node> parent = table->GetAncestor(table->get_NodeType());

    while (parent != nullptr)
    {
        depth++;
        parent = parent->GetAncestorOf<SharedPtr<Table>>();
    }

    return depth;
}

static int GetChildTableCount(SharedPtr<Table> table)
{
    int childTableCount = 0;

    for (const auto& row : System::IterateOver(table->get_Rows()->LINQ_OfType<SharedPtr<Row>>()))
    {
        for (const auto& Cell : System::IterateOver(row->get_Cells()->LINQ_OfType<SharedPtr<Cell>>()))
        {
            SharedPtr<TableCollection> childTables = Cell->get_Tables();

            if (childTables->get_Count() > 0)
            {
                childTableCount++;
            }
        }
    }

    return childTableCount;
}
```

## See Also

* Class [TableCollection](../../tablecollection/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
