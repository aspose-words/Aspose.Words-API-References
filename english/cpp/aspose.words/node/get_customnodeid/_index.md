---
title: Aspose::Words::Node::get_CustomNodeId method
linktitle: get_CustomNodeId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Node::get_CustomNodeId method. Specifies custom node identifier in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/node/get_customnodeid/
---
## Node::get_CustomNodeId method


Specifies custom node identifier.

```cpp
int32_t Aspose::Words::Node::get_CustomNodeId() const
```

## Remarks


Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

## Examples



Shows how to traverse through a composite node's collection of child nodes. 
```cpp
auto doc = MakeObject<Document>();

// Add two runs and one shape as child nodes to the first paragraph of this document.
auto paragraph = System::ExplicitCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));
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
SharedPtr<NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (const auto& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
    case NodeType::Run:
        std::cout << "Run contents:" << std::endl;
        std::cout << "\t\"" << child->GetText().Trim() << "\"" << std::endl;
        break;

    case NodeType::Shape: {
        auto childShape = System::ExplicitCast<Shape>(child);
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

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
