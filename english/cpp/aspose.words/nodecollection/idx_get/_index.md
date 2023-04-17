---
title: Aspose::Words::NodeCollection::idx_get method
linktitle: idx_get
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeCollection::idx_get method. Retrieves a node at the given index in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/nodecollection/idx_get/
---
## NodeCollection::idx_get method


Retrieves a node at the given index.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection of nodes. |
## Remarks


The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

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

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
