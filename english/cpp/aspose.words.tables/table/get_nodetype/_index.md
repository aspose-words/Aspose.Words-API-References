---
title: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: Returns Table.
type: docs
weight: 352
url: /cpp/aspose.words.tables/table/get_nodetype/
---
## Table::get_NodeType method


Returns [Table](../../../aspose.words/nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::Tables::Table::get_NodeType() const override
```


## Examples



Shows how to traverse a composite node's tree of child nodes. 
```cpp
void RecurseChildren()
{
    auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");

    // Any node that can contain child nodes, such as the document itself, is composite.
    ASSERT_TRUE(doc->get_IsComposite());

    // Invoke the recursive function that will go through and print all the child nodes of a composite node.
    TraverseAllNodes(doc, 0);
}

void TraverseAllNodes(SharedPtr<CompositeNode> parentNode, int depth)
{
    for (SharedPtr<Node> childNode = parentNode->get_FirstChild(); childNode != nullptr; childNode = childNode->get_NextSibling())
    {
        std::cout << (String(u'\t', depth)) << Node::NodeTypeToString(childNode->get_NodeType());

        // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
        if (childNode->get_IsComposite())
        {
            std::cout << std::endl;
            TraverseAllNodes(System::DynamicCast<CompositeNode>(childNode), depth + 1);
        }
        else if (System::ObjectExt::Is<Inline>(childNode))
        {
            std::cout << " - \"" << childNode->GetText().Trim() << "\"" << std::endl;
        }
        else
        {
            std::cout << std::endl;
        }
    }
}
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

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
