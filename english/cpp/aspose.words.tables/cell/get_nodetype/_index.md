---
title: Aspose::Words::Tables::Cell::get_NodeType method
linktitle: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Cell::get_NodeType method. Returns Cell in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.tables/cell/get_nodetype/
---
## Cell::get_NodeType method


Returns [Cell](../../../aspose.words/nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::Tables::Cell::get_NodeType() const override
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
            TraverseAllNodes(System::ExplicitCast<CompositeNode>(childNode), depth + 1);
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

## See Also

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
