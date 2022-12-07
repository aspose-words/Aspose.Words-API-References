---
title: TableCollection
second_title: Aspose.Words for C++ API Reference
description: Provides typed access to a collection of Table nodes. To learn more, visit the  documentation article.
type: docs
weight: 105
url: /cpp/aspose.words.tables/tablecollection/
---
## TableCollection class


Provides typed access to a collection of [Table](../table/) nodes. To learn more, visit the [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) documentation article.

```cpp
class TableCollection : public Aspose::Words::NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determines whether a node is in the collection. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Retrieves a [Table](../table/) at the given index. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all tables from the collection to a new array of tables. |
| static [Type](./type/)() |  |

## Examples



Shows how to remove the first and last rows of all tables in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

SharedPtr<TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(5, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(4, tables->idx_get(1)->get_Rows()->get_Count());

for (const auto& table : System::IterateOver(tables->LINQ_OfType<SharedPtr<Table>>()))
{
    if (table->get_FirstRow() != nullptr)
    {
        table->get_FirstRow()->Remove();
    }
    if (table->get_LastRow() != nullptr)
    {
        table->get_LastRow()->Remove();
    }
}

ASSERT_EQ(3, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(2, tables->idx_get(1)->get_Rows()->get_Count());
```


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

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words](../../)
