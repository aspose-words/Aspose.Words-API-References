---
title: Aspose::Words::CompositeNode::get_ChildNodes method
linktitle: get_ChildNodes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::get_ChildNodes method. Gets all immediate child nodes of this node in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/compositenode/get_childnodes/
---
## CompositeNode::get_ChildNodes method


Gets all immediate child nodes of this node.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::CompositeNode::get_ChildNodes()
```

## Remarks


Note, [ChildNodes](./) is equivalent to calling [GetChildNodes()](../getchildnodes/) with arguments ([Any](../../nodetype/), **false**) and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

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

## See Also

* Class [NodeCollection](../../nodecollection/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
