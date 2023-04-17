---
title: Aspose::Words::NodeCollection::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeCollection::get_Count method. Gets the number of nodes in the collection in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/nodecollection/get_count/
---
## NodeCollection::get_Count method


Gets the number of nodes in the collection.

```cpp
int32_t Aspose::Words::NodeCollection::get_Count()
```


## Examples



Shows how to traverse through a composite node's collection of child nodes. 
```cpp
auto doc = MakeObject<Document>();

// Add two runs and one shape as child nodes to the first paragraph of this document.
auto paragraph = System::DynamicCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));
paragraph->AppendChild(MakeObject<Run>(doc, u"Hello world! "));

auto shape = MakeObject<Shape>(doc, ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape->set_CustomNodeId(100);
shape->set_WrapType(WrapType::Inline);
paragraph->AppendChild(shape);

paragraph->AppendChild(MakeObject<Run>(doc, u"Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
SharedPtr<NodeCollection> children = paragraph->get_ChildNodes();

ASSERT_EQ(3, paragraph->get_ChildNodes()->get_Count());

for (const auto& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
    case NodeType::Run:
        std::cout << "Run contents:" << std::endl;
        std::cout << "\t\"" << child->GetText().Trim() << "\"" << std::endl;
        break;

    case NodeType::Shape: {
        auto childShape = System::DynamicCast<Shape>(child);
        std::cout << "Shape:" << std::endl;
        std::cout << String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
        ASSERT_EQ(100, shape->get_CustomNodeId());
        break;
    }

    default:
        break;
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

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
